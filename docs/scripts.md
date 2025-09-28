## Scripts and Behavior

This project uses Bootstrap 5 JavaScript for interactive components. No custom JS is present beyond Bootstrap.

### Included scripts
- `js/bootstrap.bundle.min.js` (recommended): Bootstrap core + Popper in one file. This is sufficient for all components used.
- `js/bootstrap.min.js`: Bootstrap core without Popper. Not needed when the bundle is included.

In `index.html` both are included:
```html
<script src="js/bootstrap.bundle.min.js"></script>
<script src="js/bootstrap.min.js"></script>
```
You can safely remove the second line to avoid duplicate initialization.

### Bootstrap components used

- Carousel (Home and Clients sections)
  - Markup uses `data-bs-ride="carousel"`, indicators, and controls.
  - Programmatic API example:
  ```html
  <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">…</div>
  <script>
    const el = document.getElementById('carouselExampleCaptions');
    const carousel = bootstrap.Carousel.getOrCreateInstance(el, { interval: 5000, ride: 'carousel' });
    // carousel.next(); carousel.prev();
  </script>
  ```

- Collapse (Navbar)
  - Toggler button controls `#navbarSupportedContent` via `data-bs-toggle="collapse"` and `data-bs-target="#navbarSupportedContent"`.
  - Programmatic example:
  ```html
  <button class="navbar-toggler" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">…</button>
  <div id="navbarSupportedContent" class="collapse navbar-collapse">…</div>
  <script>
    const target = document.getElementById('navbarSupportedContent');
    const collapse = bootstrap.Collapse.getOrCreateInstance(target);
    // collapse.show(); collapse.hide();
  </script>
  ```

### Font Awesome
- Icons are provided by `css/all.min.css` and `webfonts/`.
- Usage example:
```html
<i class="fa-brands fa-twitter"></i>
<i class="fa-solid fa-gear"></i>
```

### Best practices
- Include only `bootstrap.bundle.min.js` to reduce duplication and ensure Popper is available.
- Keep behavior declarative with `data-bs-*` attributes where possible. Use programmatic APIs for custom timing or controls.

