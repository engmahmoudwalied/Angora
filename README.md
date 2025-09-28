## Angora Landing Page – Documentation

This repository contains a static, responsive landing page built with Bootstrap 5 and Font Awesome.

### Quick start
- Open `index.html` in any modern browser.
- No build step is required.

### Project structure
- `index.html`: Main page markup (Navbar, Home/Carousel, About, Team, Services, Clients/Reviews, Contact, Footer)
- `css/`
  - `bootstrap.min.css`: Bootstrap 5 styles
  - `all.min.css`: Font Awesome icons
  - `style.css`: Custom styles for this site
- `js/`
  - `bootstrap.bundle.min.js`: Bootstrap JS (includes Popper)
  - `bootstrap.min.js`: Bootstrap JS (requires Popper)
- `images/`: Images used across sections
- `webfonts/`: Font Awesome webfonts

### Documentation
- Components and markup: `docs/components.md`
- Custom styles and variables: `docs/styles.md`
- Scripts and Bootstrap usage: `docs/scripts.md`

### Notes
- You typically only need `bootstrap.bundle.min.js` (it already includes Popper). Including both bundle and non-bundle is redundant.

