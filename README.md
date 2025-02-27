# Accessibility Prompt for Generative AI (WCAG 2.2)

This repository provides a comprehensive prompt designed for use with generative AI in 2025, aimed at fixing HTML and CSS to comply with WCAG 2.2 (WAI) accessibility requirements.

## Prompt
>"review and modify the following HTML code to ensure compliance with web accessibility requirements according to WCAG 2.2 (WAI), covering levels A, AA, and AAA. Consider the following guidelines and make the necessary modifications:
ARIA Attributes:
Ensure that all form elements (text fields, text areas, selectors, etc.) have the appropriate ARIA attributes (e.g., aria-label, aria-labelledby, aria-describedby, aria-invalid, aria-required) to describe their purpose, state, and any associated errors.
Apply ARIA roles to user interface components (buttons, links, menus, etc.) that do not use semantic native HTML elements, and use the corresponding ARIA states and properties.
Implement dynamic status messages with aria-live to notify screen reader users about content changes, especially in Single Page Applications (SPA).

HTML5 Semantics:
Use semantic HTML5 elements such as header, nav, main, article, aside, footer, and section to structure the page and define key regions.
Group related links within nav elements.

Alternative Text in Images:
Ensure that all images have descriptive alt attributes that convey the content and function of the image. If the image is purely decorative, use an empty alt attribute (alt="").

Document Structure:
Verify that the document structure is logical and hierarchical, using headings <h1> through <h6> appropriately to reflect the importance of the content.

Color Contrast:
Ensure that the color contrast between text and background meets the minimum contrast ratios specified in WCAG 2.2 (4.5:1 for normal text, 3:1 for large text and user interface elements).

Keyboard Accessibility:
Verify that all website functionality is accessible via the keyboard, ensuring a logical and visible focus order.
Avoid keyboard focus traps, where focus gets stuck in an element.
For complex interactions (such as drag and drop), provide keyboard alternatives.

Accessible Forms:
Associate <label> elements with form fields using the for attribute.
Provide clear instructions and helpful error messages for data entry.
Use the autocomplete attribute to facilitate the entry of repeated data.

Accessible Links:
Ensure that the purpose of each link is clear from the link text or surrounding context.
If the link text is not sufficiently descriptive, provide alternative text using ARIA attributes.

Adaptability and Reflow:
Ensure that the content can be reflowed and presented without loss of information or functionality, and without requiring two-dimensional scrolling.
Use media queries and Flexbox for an adaptable design.

Other WCAG 2.2 Criteria:
Review and apply all other relevant success criteria and guidelines of WCAG 2.2 for levels A, AA, and AAA. This includes, but is not limited to, providing alternatives for non-textual content, ensuring that content is adaptable, and avoiding content that causes flashes or flickers.
Please provide a revised HTML code that complies with these guidelines."

## Instructions for Use

**Adaptations and Additional Considerations:**

* **Code Context:** Provide the specific HTML code you want to review and modify to the AI.
* **Concrete Examples:** Include concrete examples of how to apply the guidelines, especially for ARIA attributes and HTML5 semantics.
* **Validation:** Ask the AI to validate the resulting code using HTML and accessibility validation tools (such as WAVE, Accessibility Insights, axe DevTools).
* **Screen Reader Testing:** Request that the code be tested with a screen reader (such as NVDA, JAWS, or VoiceOver) to verify the correct interpretation of elements and ARIA attributes.
* **Flexibility:** Allow the AI to propose alternative solutions that comply with accessibility requirements, as long as they are justified and consistent with WCAG 2.2.
* **PDF Documents:** If generating PDF documents, ensure they are also accessible.
* **Single Page Applications (SPA):** Pay special attention to accessibility in SPAs.

**Example of Application in an IDE:**

1.  Copy the prompt above.
2.  Open the HTML file you want to modify in your IDE (e.g., Visual Studio Code).
3.  Activate your programming assistant (e.g., GitHub Copilot).
4.  Paste the prompt into the assistant panel, including the HTML code you want to review.
5.  Review the AI's suggestions and apply the relevant modifications.
6.  Validate the resulting code with the tools mentioned above and perform tests with a screen reader.

This prompt, along with the adaptations and additional considerations, should provide a clear and effective guide for a programming assistant to modify HTML code and comply with accessibility requirements according to WCAG 2.2.

## Example: Code with Accessibility Issues

This section highlights common accessibility issues found in poorly written HTML.

**Bad Practices:**

* Lack of proper semantic tags (e.g., `<h1>` without clear structure).
* Forms without associated `<label>` elements or `for` attributes.
* Tables without header cells (`<th>`).
* Images without `alt` attributes.
* Links with non-descriptive text.
* Non-accessible elements like `<div>` used as buttons.
* Hidden content that is not detectable by screen readers.
* Incorrect heading hierarchy (e.g., `<h4>` followed by `<h3>`).
* Low color contrast (e.g., light gray text on a light gray background).
* Links without visible focus states.
* Use of color alone to convey information (e.g., error messages).
* Videos without captions or alternative descriptions.
* Empty buttons without text or `aria-label`.
* Poorly structured forms with unclear labels.
* Misuse of bold and italic tags (`<b><i>`) without structural purpose.
* Generic link text ("Click here").

## Example: Fixed Code with Accessibility Improvements

This section details the accessibility improvements made to the example code.

**Implemented Accessibility Changes:**

* **Semantic Structure:**
    * Implemented HTML5 semantic elements (`<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`).
    * Added a "skip to content" link for keyboard users.
    * Correctly organized headings (`<h1>`, `<h2>`) in hierarchical order.
* **ARIA Attributes:**
    * Included `aria-label`, `aria-labelledby`, and `aria-describedby` attributes.
    * Added appropriate ARIA roles (e.g., `role="alert"`, `role="status"`).
    * Implemented dynamic regions with `aria-live` for notifications.
* **Forms:**
    * Associated `<label>` elements with form fields using `for` attributes.
    * Added `fieldset` and `legend` to group related fields.
    * Included `autocomplete` attributes.
    * Provided visual indicators for required fields.
* **Multimedia:**
    * Added descriptive `alt` attributes for images.
    * Implemented captions and descriptions for videos.
    * Included `figcaption` for image context.
* **Contrast and Color:**
    * Improved text and background contrast (minimum ratio 4.5:1).
    * Eliminated the use of color alone to convey information.
    * Added additional visual indicators (icons, borders).
* **Keyboard Navigation:**
    * Ensured all interactive elements are keyboard accessible.
    * Implemented visible focus states.
    * Created a logical and predictable tab order.
* **Tables:**
    * Added appropriate table headers with `<th>` and `scope` attributes.
    * Included `<caption>` to describe the table's purpose.
    * Correctly structured with `<thead>` and `<tbody>`.
* **Links:**
    * Replaced generic links with descriptive text.
    * Ensured all links have a clear purpose from their text.

This code is now optimized for use with assistive technologies like screen readers and complies with WCAG 2.2 accessibility requirements at levels A, AA, and AAA.
