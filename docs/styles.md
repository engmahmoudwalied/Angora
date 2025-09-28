### Styles API

This template exposes theme-level settings via CSS Custom Properties and provides utility classes for common styling actions.

#### CSS Custom Properties (Theme Variables)

| Name | Default | Purpose |
|---|---|---|
| `--main-color` | `#f25454` | Primary accent color (buttons, hovers, highlights) |
| `--heading-color` | `#282828` | Headings color (`h1`–`h6`) |
| `--color-gray` | `#666` | Base body text color |
| `--color-gray-2` | `#444` | Secondary/darker gray for headings and indicators |
| `--fw-700` | `700` | Bold font weight used in headings |
| `--fw-600` | `600` | Semi-bold weight used in nav and titles |
| `--fw-500` | `500` | Medium weight for subtle emphasis |
| `--transition` | `all .5s ease` | Default transition for interactive elements |
| `--custome-font` | `'Poppins', sans-serif` | Display font for certain sections |
| `--normal-font` | `'Open Sans', sans-serif` | Body font |

Override any variable by redefining it after `style.css` is loaded, or by editing `:root` in `css/style.css`.

```css
/* Example: change the primary accent color */
:root {
  --main-color: #1e90ff;
}
```

#### Global Typography
- Body uses `--normal-font`, color `--color-gray`, line-height `1.75em`.
- `h1`–`h6` use `--heading-color` and weight `--fw-600`.

#### Utilities
- **`.custome-color`**: Applies `--main-color` to text.
- **`.lead`**: Sets a medium paragraph size/leading for highlighted text blocks.
- **`.main-btn`**: Primary button style; hover uses a lighter variant of `--main-color`.
- **`.tag`**: Pill-like link style used in the footer tag cloud.

Usage example:

```html
<button class="main-btn rounded">Call To Action</button>
<span class="custome-color">Highlighted text</span>
```

#### Responsive Behavior
Key breakpoints:
- `@media (max-width: 991px)`: Navbar collapses; `.in` class styles the opened menu panel.
- `@media (max-width: 767px)`: Smaller hero heading; reviews expand to full width; info box stacks.

