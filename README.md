# MyBike Landing Page

A responsive landing page implemented from the MYBIKE Figma design.

- [DEMO LINK](https://bcheban.github.io/mybike_landing-page/)
- [MYBIKE design](https://www.figma.com/file/NZQAIydtHo5QkINyGLHNcq/BIKE-New-Version?node-id=0%3A1)

# Technologies used

- HTML5
- SCSS (Sass) with BEM methodology
- Vite

# Getting started

1. Clone the repository:
   ```bash
   git clone https://github.com/bcheban/mybike_landing-page.git
   cd layout_landing-page
   ```
2. Install dependencies (Node.js `v20` recommended):
   ```bash
   npm install
   ```
3. Run the project locally:
   ```bash
   npm start
   ```
4. Build for production:
   ```bash
   npm run build
   ```
5. Deploy to GitHub Pages:
   ```bash
   npm run deploy
   ```

# Tips & Hints

- Check `background-image: url()` paths to be relative to `main.scss` — they should start with `../images`.
- If some points from the checklist below are not relevant to your design, just skip them.

# Checklist

1. Use the logo as a favicon.
2. Use the landing name as a page title.
3. All logos should be links to the top of the page.
4. Change text color on hover for phone, email, and address.
5. Make sure phone icons and phone numbers are real links to start a call.
6. All addresses should be links to some location on Google Maps. Open them in a new tab with `target="_blank"`.
7. Increase all images on hover (make them links to `#`, if there is no better option).
8. Make sure everything looks neat on mobile and without horizontal scrolling.
9. The speed of animations should be the same throughout the page (for example, increasing when hovering or moving blocks when scrolling).
10. Ensure that all `nav__link`s work smoothly.
11. Disable page scrolling under the menu using the following code:
    ```css
    .page:has(.page__menu:target) {
      overflow: hidden; /* not to scroll the page */
    }
    ```
12. Make it possible to scroll the menu if it is higher than the viewport:
    ```css
    .menu {
      overflow: auto; /* to scroll the menu if needed */
    }
    .menu__top {
      position: sticky; /* to keep cross always visible */
      top: 0;
      z-index: 1;
      background-color: #e5e5e5;
    }
    ```
13. All form fields should be required and have correct types (`email`, `tel`, etc.).
14. Placeholders should give examples of what should be added, to make the expected format clear.
15. The page shouldn't be reloaded on form submit, but the fields should be cleared. Use:
    ```html
    <form onsubmit="this.reset(); return false;">
    ```
16. Make the `footer` sticky at the bottom with `z-index: -1` to get a `fixed` background effect.
