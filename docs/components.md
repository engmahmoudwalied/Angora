## Components and Markup

This page documents the public structure and reusable markup patterns in `index.html` and how to use or extend them.

### Navbar
- Selector: `nav.navbar#navbar`
- Purpose: Site navigation with brand logo, section links, and social icons.
- Key classes/IDs:
  - `#logo`: Brand image inside `.navbar-brand`
  - `.navbar-toggler` with `data-bs-toggle="collapse"`, `data-bs-target="#navbarSupportedContent"`
  - `#navbarSupportedContent`: Collapsible container (Bootstrap collapse)
  - `.nav-icons`: Social links container
- Behavior: Collapses to a toggler on small screens. Active link styled via `.nav-link.active`.
- Example:
```html
<nav class="navbar navbar-expand-lg navbar-dark fixed-top" id="navbar">
  <div class="container">
    <a class="navbar-brand" href="#"><img src="images/logo1.png" alt="logo" id="logo"></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse in" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
        <li class="nav-item fw-600"><a class="nav-link active" href="#home">Home</a></li>
        <!-- more links -->
      </ul>
      <div class="nav-icons"><a href="#"><i class="fa-brands fa-twitter"></i></a></div>
    </div>
  </div>
  </nav>
```

### Home / Hero Carousel
- Selector: `section.home` containing `.carousel` (id: `#carouselExampleCaptions`)
- Purpose: Full-width hero slider with captions.
- Bootstrap APIs used: Carousel with indicators and controls.
- Example minimal slide:
```html
<section class="home" id="home">
  <div id="carouselExampleCaptions" class="carousel slide" data-bs-ride="carousel">
    <div class="carousel-inner">
      <div class="carousel-item active">
        <img src="images/background.jpg" class="d-block w-100" alt="">
        <div class="caption"><h1>We build great brands.</h1></div>
      </div>
    </div>
  </div>
</section>
```

### About
- Selector: `section.about`
- Purpose: Company description and skill progress bars.
- Structure:
  - `.title-section` with `h2`, `hr`, and intro paragraph.
  - `.desc .lead` paragraphs.
  - `.skills` list of `.bar` items:
    - `.progress-heading` wrapping `.progress-title` and `.progress-value`
    - `.progress > .progress-bar` with inline `style="width: X%"`

### Team
- Selector: `section.team`
- Purpose: Team members grid with hover overlay and social icons.
- Card structure (`.member-box`):
  - `.member-img` (contains `<img>` and overlay `.member-img-layer` with icons)
  - `.member-details` with `<h5>` name and `.title-job` role

### Info Callout
- Selector: `section.info`
- Purpose: Full-width call-to-action bar with heading and button.
- Structure: `.info-box` wraps `<h3>` and `.main-btn` button.

### Services
- Selector: `section.services`
- Purpose: Feature/service grid.
- Item structure (`.service-box`):
  - `.service-icon.custome-color` with Font Awesome `<i>`
  - `.content` with `<h3>` and paragraph

### Clients / Reviews
- Selector: `section.clients`
- Purpose: Client testimonials in a Bootstrap carousel (`#carouselExampleIndicators`).
- Slide structure: `.client-box` with `.client-img`, `.client-info`, and `.review`.

### Contact
- Selector: `section.contact`
- Purpose: Contact details and a static form UI.
- Left: `.contact-details` list of `.contact-content` items (Address, Phone, Email)
- Right: `.form-contact > form` with inputs and `.main-btn` submit button.

### Footer
- Selector: `footer.footer`
- Purpose: Footer widgets, tags, social icons, back-to-top.
- Elements:
  - `.to-top` anchor with chevron icon
  - `.footer-widgets` with four `.widget` columns
  - `.copy-right` with social icons and copyright text

### Section IDs and nav anchors
- Supported IDs for deep links: `#home`, `#about`, `#team`, `#projects` (no section present by default), `#services`, `#blog` (no section present by default), `#contact`, `#clients`.
- To add a new section: create `<section id="your-id">…</section>` and add a corresponding navbar link.

