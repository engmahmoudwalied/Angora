### Components API

Each section in `index.html` is a reusable component composed from Bootstrap and custom classes defined in `css/style.css`. Below are the public structures and hooks you can use.

#### Navbar
- Sticky, collapsible navigation bar with social icons.
- Key classes: `navbar`, `navbar-expand-lg`, `navbar-dark`, `fixed-top`, `nav-link`, `nav-icons`.

Minimal structure:

```html
<nav class="navbar navbar-expand-lg navbar-dark fixed-top" id="navbar">
  <div class="container">
    <a class="navbar-brand" href="#"><img src="images/logo1.png" alt="logo" id="logo"></a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse in" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
        <li class="nav-item"><a class="nav-link active" href="#home">Home</a></li>
        <!-- ... more links ... -->
      </ul>
      <div class="nav-icons">
        <a href="#"><i class="fa-brands fa-twitter"></i></a>
        <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
        <a href="#"><i class="fa-brands fa-instagram"></i></a>
      </div>
    </div>
  </div>
</nav>
```

Notes:
- The `.in` class styles the expanded mobile menu panel below 991px width.
- Use `nav-link active` to highlight the current section.

#### Home (Hero Carousel)
- Bootstrap carousel with full-bleed background images and centered caption.
- Key classes: `home`, `carousel`, `carousel-inner`, `carousel-item`, `caption`.

Add a slide:

```html
<div class="carousel-item">
  <img src="images/bg2.jpg" class="d-block w-100" alt="...">
  <div class="caption"><h1>Your headline</h1></div>
</div>
```

#### About
- Split layout with descriptive text and animated skill bars.
- Key classes: `about`, `bar`, `progress-heading`, `progress`, `progress-bar`, `progress-title`, `progress-value`.

Skill bar block:

```html
<div class="bar">
  <div class="progress-heading" style="width: 80%">
    <p class="progress-title float-start m-0">Branding</p>
    <span class="progress-value float-end">80%</span>
    <div class="clearfix"></div>
  </div>
  <div class="progress"><div class="progress-bar" style="width: 80%"></div></div>
</div>
```

#### Team
- Grid of team member cards with hover overlay and social icons.
- Key classes: `team`, `member-box`, `member-img`, `member-img-layer`, `member-details`.

Member card:

```html
<div class="member-box">
  <div class="member-img position-relative">
    <img src="images/man1.jpg" class="w-100" alt="member">
    <div class="member-img-layer d-flex justify-content-center align-items-center text-white">
      <i class="fa-brands fa-twitter"></i>
      <i class="fa-brands fa-facebook-f"></i>
      <i class="fa-brands fa-linkedin-in"></i>
      <i class="fa-brands fa-dribbble"></i>
    </div>
  </div>
  <div class="member-details text-center">
    <h5 class="m-0">Member Name</h5>
    <span class="title-job">Job Title</span>
  </div>
</div>
```

#### Info (CTA)
- Centered call-to-action band with button.
- Key classes: `info`, `info-box`, `main-btn`.

```html
<div class="info-box d-flex justify-content-md-around align-items-center justify-content-center">
  <h3 class="mb-3 mb-md-0">Do you have any ideas?</h3>
  <button class="main-btn rounded">Contact Us</button>
</div>
```

#### Services
- Icon + text feature boxes in a responsive grid.
- Key classes: `services`, `service-box`, `service-icon`, `content`.

Service box:

```html
<div class="service-box d-flex">
  <div class="service-icon custome-color"><i class="fa-solid fa-display"></i></div>
  <div class="content">
    <h3>Responsive Layout</h3>
    <p class="m-0">Short description here.</p>
  </div>
</div>
```

#### Clients (Reviews Carousel)
- Bootstrap carousel with client avatars and quotes.
- Key classes: `clients`, `client-box`, `client-img`, `client-info`, `review`.

Client item:

```html
<div class="carousel-item">
  <div class="client-box text-center">
    <div class="client-img"><img src="images/client-2.png" class="rounded-circle" alt="Client Review"></div>
    <div class="client-info"><h3>Client Name</h3><span>Company</span></div>
    <div class="review m-auto position-relative">
      <p><i class="fa-solid fa-quote-left"></i> Your quote here <i class="fa-solid fa-quote-right"></i></p>
    </div>
  </div>
</div>
```

#### Contact
- Two-column layout with contact details and a basic form.
- Key classes: `contact`, `contact-details`, `contact-content`, `form-contact`, `form-control`, `main-btn`.

Form block:

```html
<form>
  <input type="text" class="form-control" placeholder="Name">
  <input type="email" class="form-control" placeholder="Email">
  <input type="text" class="form-control" placeholder="Phone">
  <textarea class="form-control" placeholder="Message" rows="3"></textarea>
  <button class="main-btn rounded"><i class="fa-solid fa-paper-plane"></i> Send Message</button>
</form>
```

#### Footer
- Widgetized footer with tags and a centered "back to top" control.
- Key classes: `footer`, `footer-widgets`, `widget`, `tag`, `to-top`, `copy-right`.

Back to top control:

```html
<a href="#" class="to-top"><i class="fa-solid fa-chevron-up"></i></a>
```

