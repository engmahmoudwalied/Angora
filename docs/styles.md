## Custom Styles and Variables

All custom CSS lives in `css/style.css`. It augments Bootstrap and defines site-specific variables and components.

### CSS Variables (root)
- `--main-color`: Primary accent (`#f25454`)
- `--heading-color`: Heading color (`#282828`)
- `--color-gray`, `--color-gray-2`: Body and secondary text
- Font weights: `--fw-600`, `--fw-700`, `--fw-500`
- `--transition`: Default transition (`all .5s ease`)
- Fonts: `--custome-font` (`Poppins`), `--normal-font` (`Open Sans`)

Usage example:
```css
.custome-color { color: var(--main-color); }
```

### Global typography
- `body`: sets base font family/size/line-height
- `h1..h6`: heading color and weight
- `.lead`: smaller paragraph sizing override

### Navbar
- `.navbar`: padding, border, transition
- `.navbar-dark .nav-link` vs `.navbar-light .nav-link` colors
- `.nav-link.active` and hover use `--main-color`
- Responsive behavior (`@media max-width: 991px`):
  - `.in`: styles collapsed menu container (white background, absolute position)

### Home / Carousel
- `.caption`: full overlay center alignment; `.caption h1` large font
- `.carousel-control-*`: visible controls styled with borders and hover layers
- Scroll cue: `.home .scroll` with `@keyframes scroll`

### About – Skills
- `.bar .progress-heading`, `.progress-title`, `.progress-value`
- `.progress` height and background; `.progress-bar` uses `--main-color`

### Team
- `.member-img` overflow hidden; zoom on `.member-box:hover img`
- `.member-img-layer`: overlay appears on hover with social icons
- `.member-details h5`: hover color swap to `--main-color`

### Info section
- `.main-btn`: primary CTA button, hover lightens color
- Responsive: `.info-box` stacks on small screens

### Services
- `.service-box` spacing; hover changes `<h3>` color to main accent

### Clients / Reviews
- `.client-img img`: fixed size circle via `rounded-circle` in HTML and size overrides here
- `.review`: fixed width with responsive fallback at `max-width: 767px`
- `.carousel-indicators [data-bs-target]`: custom indicators styling

### Contact
- `.contact-details` headings and borders
- `.form-control:focus`: accent border and box-shadow using `--main-color`

### Footer
- `.footer-widgets`: background image, padding
- `.to-top`: circular floating button; hover accent
- `.widget h5`, `.widget a`, `.tag` styles with hover interactions
- `.copy-right`: dark bar with social icon hover colors

### Adding new styles
1. Prefer variables from `:root` for color/typography/transition consistency.
2. Add section-scoped classes (e.g., `.portfolio`) and keep selectors shallow.
3. Maintain responsive behavior with mobile-first media queries.

