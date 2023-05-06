A list of common principles & practices for creating UI on the web.

---

## Layout

* For most web layouts, a 1-dimensional method like [Flexbox](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox) works well.
* When 2-dimensional space is needed, prefer a more robust layout option like [CSS Grid](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Grids).
* Use [@media rules](https://developer.mozilla.org/en-US/docs/Web/CSS/@media) to adapt layouts based on device conditions, such as viewport width.
* Understand the impact of [whitespace](https://uxplanet.org/the-power-of-whitespace-a1a95e45f82b) on layout and readability.
* Leverage [proximity](https://en.wikipedia.org/wiki/Principles_of_grouping#Proximity) to communicate content relationships and to form visual hierarchies between elements.

## Color

* Be consistent with the use of color across similar elements and throughout the overall UI.
* Prefer dark text on light backgrounds and light text on dark backgrounds.
* Use a contrast ratio of at least 4.5:1 for small text (17 pt and below).
* Use a contrast ratio of at least 3:1 for large text (18 pt and up).
* Use variables to reference colors. Prefer using [CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_custom_properties) to cascade inheritance down the document.
* Pick colors considerately, and within the context of an overall theme or brand.

### References

1. [Contrast - World Wide Web Consortium (W3C)](https://www.w3.org/TR/WCAG21/#contrast-minimum)

2. [Use of Color - World Wide Web Consortium (W3C)](https://www.w3.org/WAI/WCAG21/Understanding/use-of-color.html)

3. [Color - US Web Design System](https://designsystem.digital.gov/design-tokens/color/overview/)

## Typography

* Prefer highly readable fonts like Roboto, serif, or sans-serif.
* Do not use more than three different fonts within a single application.
* Create typographic hierarchy through font weight, size, and case. Consider use of a type scale.
* Use letter spacing to improve readability.
* Prefer a maximum line length of 50 to 60 characters - including spaces.

### References

1. [Typography - Adobe Blog](https://blogs.adobe.com/creativecloud/xd-essentials-typography-in-mobile-apps/)
2. [Type Scale - Material Design](https://material.io/design/typography/#type-scale)

## Buttons

* Use a simple verb or short verb phrase with title-style capitalization for the button text. For example, "Send Payment".
* Group related buttons to convey their relationship.
* When multiple buttons are grouped together, give them all the same height and enough space between them.
* Consider filled buttons to emphasize high significance, outlined buttons for medium significance, and text buttons for lower significance.
* Use a noticeable destructive style for buttons which have a destructive consequence, such as deleting data.

### References

1. [Buttons - Material Design](https://material.io/components/buttons/)
2. [Buttons - GNOME Developer](https://developer.gnome.org/hig/stable/buttons.html.en)

## Forms & Input

* Indicate required fields explicitly, for example with an asterisk (\*).
* Order the form logically.
* Prefer a single column for forms. The path to completion should be a straight line down the page.
* Use autofocus (tabindex) to communicate the starting point of the form.
* Use short but descriptive labels. Ideally just 1 or 2 words.
* Use top aligned labels if you want the form to be quickly scanned. Use left aligned labels if you want users to read carefully.
* Position search boxes in the upper right so users may find it where they expect.
* Provide visual feedback upon form submission to indicate a form is being processed and to prevent duplicate posts.
* Use right aligned labels for checkbox inputs to yield better scannability.

### References

1. [Designing more efficient forms - UX Planet](https://uxplanet.org/designing-more-efficient-forms-structure-inputs-labels-and-actions-e3a47007114f)

## Data Visualization

* Prefer 5 or fewer slices in a pie or donut chart.
* Prefer a horizontal bar chart when a dataset contains long labels. Truncate labels if needed.
* Use the x-axis to plot time metrics (time should flow left to right).
* Presort datasets to improve readability.
* Include a title for the visualization in the upper left corner.
* Include any controls in the upper right corner.
* Implement sorting and filtering to give users control over how the data is displayed in tables.
* Always indicate when data is missing.

### References

1. [Data Visualization - Material Design](https://material.io/design/communication/data-visualization.html)
2. [Charts - UX Design](https://uxdesign.cc/designing-charts-principles-every-designer-should-know-5bd3969a0150)

## Interaction & Feedback

* Confirm & acknowledge important user actions to reduce uncertainty for the user and to prevent mistakes.
* Avoid unnecessary alerts as they are inherently disruptive. Only use alerts to deliver important, and ideally actionable, information.
* Error messages should
  * Identify the problem
  * Provide details (if helpful)
  * Guide the user towards a solution (if possible)
  * Be highly visible
* Use visual affordance cues to indicate the state of UI elements. Be consistent with cues across similar components.
  * *types of state*: Hover, Enabled, Disabled, Focused, Selected, Activated, Pressed, On, Off, Loading, Error.

### References

[States & Interaction - Material Design](https://material.io/design/interaction/states.html)

## UX Principles

[Principles of Grouping](https://en.wikipedia.org/wiki/Principles_of_grouping): Humans naturally perceive objects as organized patterns and objects.

[Principle of Least Astonishment](https://en.wikipedia.org/wiki/Principle_of_least_astonishment): Parts of a system should behave in ways that users expect.

[Hick's Law](https://www.interaction-design.org/literature/article/hick-s-law-making-the-choice-easier-for-users): The time it takes to make a decision increases with the number and complexity of choices.

[Miller's Law](https://lawsofux.com/millers-law): The average person can only keep 7 (plus or minus 2) items in their working memory.

[Aesthetic–usability effect](https://en.wikipedia.org/wiki/Aesthetic%E2%80%93usability_effect): Users often perceive aesthetically pleasing design as design that’s more usable.

[Serial Position Effect](https://www.interaction-design.org/literature/topics/serial-position-effect): Users have a tendency to best remember the first and last items in a series.

[Zeigarnik Effect](https://lawsofux.com/zeigarnik-effect): People remember uncompleted or interrupted tasks better than completed tasks.

[Von Restorff Effect](https://lawsofux.com/von-restorff-effect): When multiple similar objects are present, the one that differs from the rest is most likely to be remembered.

## Developer Tools

* [Contrast validator](https://color.review/)
* [AXE Chrome Accessibility extension](https://www.deque.com/axe/)
* [Color Palette generator](https://material.io/resources/color)
