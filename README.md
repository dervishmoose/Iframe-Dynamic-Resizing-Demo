
# Iframe Dynamic Resizing Demo

This project demonstrates how to embed a form inside an iframe and automatically adjust the iframe's height based on its content and interactions. This solution ensures that the iframe is responsive and adapts to content changes (such as user input or AJAX updates) and window resizing, preventing scrollbars and maintaining a clean user experience. (i.e. This is a simple way to make your iframes both mobile responsive and content responsive. This code makes a form look like it is directly on a page and not included in an iFrame. )

**Important:** This solution requires adding code to both the parent page (the page where the iframe is embedded) and the iframe page (the page being displayed inside the iframe). So, you will need to have access to both pages. Sorry, there is no magic bullet to do only from the parent page.


## Demo
Let's get right to it:
[See the Iframe Dynamic Resizing Demo](https://dervishmoose.github.io/Iframe-Dynamic-Resizing-Demo)


## Project Overview

### What is it?
This is a demo that showcases an embedded form inside an iframe that resizes dynamically based on user interactions and window resizing. The form adapts to different inputs, such as selecting different payment options, and adjusts the iframe's height accordingly. The iframe content and the parent page communicate using the `postMessage` API to ensure the correct height is set on the parent page.

### Problem It Solves
In many situations, when embedding content in iframes, the content inside the iframe may change in size based on user interaction, form submission, or dynamic data loading (like AJAX). If the iframe’s height remains fixed, this can cause issues such as:

- **Scrollbars** inside the iframe, which can be visually unappealing.
- **Content cut-off**, where users cannot see all the content unless they manually scroll inside the iframe.
  
This demo solves these issues by:

- Automatically adjusting the iframe's height to fit the content inside.
- Supporting dynamic content changes, such as form field visibility changes or window resizing.
- Handling mobile responsiveness by adjusting the iframe height when the window is resized.

### Why Use This?
Developers embedding third-party content or forms in iframes often face issues where the iframe content changes size dynamically, but the parent page does not adjust accordingly. This solution allows you to:

- Ensure that your embedded content fits perfectly without unnecessary scrollbars.
- Provide a responsive, seamless user experience across all devices and window sizes.
- Easily handle forms or other interactive content embedded within an iframe.

## Instructions

### Prerequisites
- A basic web server (e.g., using GitHub Pages, or any HTTP server) to serve the form.
- Ensure that the `form.html` page is hosted on the server (or served locally for testing).

### How It Works
The project consists of two files:

1. **`index.html`**: The parent page where the iframe is embedded.
2. **`form.html`**: The form that is embedded within the iframe, which dynamically resizes based on user interaction or window changes.

### Instructions for Use

#### 1. File Structure

```bash
iframe-dynamic-resizing-demo/
│
├── index.html      # Parent page that embeds the form via an iframe
├── form.html       # The dynamically resizing form
└── README.md       # Documentation for the project
```

#### 2. Embedding the Iframe

To embed the iframe, the `index.html` file includes an `<iframe>` element that loads the `form.html`:

```html
<iframe id="dynamic-iframe" src="form.html" style="width:100%; border:none;"></iframe>
```

- **Dynamic Resizing**: The iframe communicates with the parent page via `postMessage`, and its height is dynamically adjusted based on the content inside the iframe.

#### 3. How to Use

1. Open `index.html` in your browser.
2. The page displays an iframe containing the `form.html` page.
3. Interact with the form by selecting different payment methods from the dropdown.
   - When you select "Credit Card," it will display credit card fields.
   - When you select "Bank," it will show the bank account field.
   - Selecting "Other" will show a single input field for additional details.
4. The iframe's height will adjust automatically based on the fields displayed.
5. **Responsive Test**: Resize the browser window to see the iframe adjust dynamically to fit the content.

### Example Use Case

Let’s say you are developing an application that integrates with third-party services or dynamically generated forms. You want to ensure that the iframe, which contains embedded content, resizes correctly as the user interacts with the form or the page resizes due to responsiveness. This solution will help you create a seamless experience without worrying about iframe scrollbars or incomplete content visibility.

### Features
- **Dynamic Height Adjustment**: The iframe adjusts its height based on the visible content, ensuring that no content is cut off.
- **Supports Mobile Responsiveness**: The iframe resizes based on the window size, making it perfect for mobile-friendly applications.
- **Handles Dynamic Content**: Works with dynamic form changes, such as revealing or hiding fields based on user interaction.

### Troubleshooting
- **Content Not Resizing Properly**: Ensure that the `form.html` is correctly loaded inside the iframe, and that both pages are served under the same domain or allowed via CORS.
- **Scrollbars Still Appear**: If scrollbars appear, check the browser’s developer console for errors related to `postMessage` or styling conflicts (such as fixed heights on iframe containers).

### Customization
- You can easily modify the `form.html` to fit your own form needs (e.g., adding more input fields or different types of interactive content).
- The `index.html` file can also be customized to fit your website’s layout or style.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

---

## Contributing

If you would like to contribute to this project, please fork the repository and submit a pull request with your changes. Any improvements to the form demo or the iframe resizing logic are welcome!

---

## Contact

For any questions or issues, please contact the project maintainer at [dervishmooseconsulting.com/contact](https://dervishmooseconsulting.com/contact/) or open an issue on the GitHub repository.
