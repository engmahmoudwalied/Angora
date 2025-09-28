### JavaScript & Behavior Guide

This site relies on Bootstrap for interactivity. There is no custom JavaScript in this repository; components work via Bootstrap's data attributes and bundled scripts.

#### Included scripts
- `js/bootstrap.bundle.min.js`: Bootstrap JS + Popper (preferred).
- `js/bootstrap.min.js`: Bootstrap without Popper (included but not necessary if bundle is used).

Ensure the bundle is included before the closing `</body>` tag (already done in `index.html`).

#### Common behaviors
- **Navbar toggler**: Controlled by `data-bs-toggle="collapse"` and `data-bs-target="#navbarSupportedContent"` on the toggler button.
- **Carousel**: `data-bs-ride="carousel"` auto-initializes the hero carousel. Slides use `.carousel-item` with one `.active` at load.
- **Indicators/Controls**: Indicators use `data-bs-target` and `data-bs-slide-to`. Prev/Next buttons use `data-bs-target` and `data-bs-slide`.

#### Programmatic control (optional)
If you add custom scripts later, you can access Bootstrap components via JS:

```html
<script>
  const carouselEl = document.querySelector('#carouselExampleCaptions');
  const carousel = new bootstrap.Carousel(carouselEl, { interval: 5000 });
  // carousel.next(); carousel.prev();
</script>
```

