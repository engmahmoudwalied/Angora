### Getting Started

This project is a static website. No build tools or package managers are required.

#### Run locally
- **Option 1**: Open `index.html` directly in your browser.
- **Option 2**: Serve the folder with a simple local server:

```bash
cd /workspace
python3 -m http.server 8000
# Open http://localhost:8000/
```

#### Directory structure
```text
/css
  bootstrap.min.css
  all.min.css
  style.css              # Project styles (CSS variables, components)
/images                  # Images used across sections
/js
  bootstrap.bundle.min.js
  bootstrap.min.js
/webfonts                # Font Awesome webfonts
index.html               # Page markup (all sections/components)
```

#### Dependencies
- **Bootstrap**: styles and components (carousel, navbar, grid). `bootstrap.bundle.min.js` includes Popper for interactive components.
- **Font Awesome**: icons (social links, service icons, etc.).

Both dependencies are already included via local assets in `index.html`.

#### Customization
- Colors, fonts, and transitions are exposed via CSS Custom Properties in `css/style.css` (see Styles API).
- Sections and blocks are composed of reusable CSS classes (see Components API).

