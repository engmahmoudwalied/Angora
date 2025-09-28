### Examples & Recipes

Copy‑paste examples for common tasks.

#### Add a new Service item
```html
<div class="col-md-6 col-lg-4">
  <div class="service-box d-flex">
    <div class="service-icon custome-color"><i class="fa-solid fa-sliders"></i></div>
    <div class="content">
      <h3>New Feature</h3>
      <p class="m-0">Describe the benefit in one or two sentences.</p>
    </div>
  </div>
</div>
```

#### Add a new Team member
```html
<div class="col-lg-3 mb-2 mb-lg-0">
  <div class="member-box">
    <div class="member-img position-relative">
      <img src="images/new-member.jpg" class="w-100" alt="member">
      <div class="member-img-layer d-flex justify-content-center align-items-center text-white">
        <i class="fa-brands fa-twitter"></i>
        <i class="fa-brands fa-facebook-f"></i>
        <i class="fa-brands fa-linkedin-in"></i>
        <i class="fa-brands fa-dribbble"></i>
      </div>
    </div>
    <div class="member-details text-center">
      <h5 class="m-0">Alex Doe</h5>
      <span class="title-job">Product Designer</span>
    </div>
  </div>
</div>
```

#### Add a new Client review (carousel slide)
```html
<div class="carousel-item">
  <div class="client-box text-center">
    <div class="client-img"><img src="images/client-4.png" class="rounded-circle" alt="Client Review"></div>
    <div class="client-info"><h3>Jamie Lee</h3><span>From Pied Piper</span></div>
    <div class="review m-auto position-relative">
      <p><i class="fa-solid fa-quote-left"></i> Loved working with your team! <i class="fa-solid fa-quote-right"></i></p>
    </div>
  </div>
</div>
```

#### Change the theme color
```css
/* Edit :root in css/style.css or override after it */
:root { --main-color: #00b894; }
```

#### Create a primary action button
```html
<button class="main-btn rounded">Get Started</button>
```

