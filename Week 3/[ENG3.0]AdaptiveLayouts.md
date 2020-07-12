# Adaptive Layouts

This lesson explains how to make your content's position adapt to your screen size

**Learning objectives

* TNTs will learn how to layout a table with React
* TNTs will understand the basics of CSS Flexbox layout
* TNTs will practice experimenting with and troubleshooting CSS in the browser

## Time required and pace

Total time: 2 hours, 30 minutes

- 45 minutes - **Pre-session**): background learning, research, and investigations
- 30 minutes - **Instructional Session**
  - 5 minutes - Discussion in groups
  - 10 minutes –  Layout using HTML Tables
  - 10 minutes - Layout using CSS Flexbox
  - 5 minutes - Exercise Setup
- 45 minutes - **Post-session**: pair programming Exercise

## Pre-session (45 minutes)

*Prepare for the session* [here](../../../wiki/[ENG2.2]View-component-layout)

## Session Details

Work through the YourShare Account page together to investigate the following topics:

### Adaptive Layouts with YourShare (20 minutes)

**GOAL**: Create a React app UI that feels "right" for [desktop and mobile users](./[ENG3.0]YourShar-layout.pdf)

1. **Identify Components**: Brand, Signup, Nav
2. **Design UI layout**: based on screen limitations and user expectations for mobile / desktop 
3. **Define layout strategy**: using CSS grid (macro) and flexbox (micro) for adaptive layout
4. **Implement adaptive layout**: using CSS cascading, media queries, and relative sizing

### Cascading Style Sheets - CSS (10 minutes)

- Style Sheets consist of **Selectors** & **Declarations** (aka “styles”)
- "***Cascading***" **Style Sheet** refers to the predictable way the browser will combine styles from different selectors onto an HTML element, choosing the "winning" set of styles based on the order and specificity of their selector. 

### Media Queries (15 minutes)

In addition to selectors and styles, CSS also provides **functions** and **imperatives** (rules) that allow it to dynamically adjust which styles are applied. Most important here is the **@media** rule (aka *a media query*) with a max or min width condition

- **max-width:** *view is **at most** ...*
- **min-width:** *view is **at least** ...*

The rule  `@media( max-width:425px ){ ...styles... }` will only apply the styles inside the curly braces when the view's **width is at most 425px**. On any larger view, the browser will ignore these styles.

Though you can combine conditions using `and`, `or` and `not` to create more complicated conditions, usually *cascading* the styles is simpler.

### Relative Sizes (10 minutes)

When assigning a size to an element we typically use fixed units like pixels or inches. However for dynamic UI layout, we most often use **Relative Sizing** for images, layout containers, and font sizes. The relative units allow the items to display differently according to the size of their parent element, root element, or the viewport (screen size).

1. **vw/vh** : Size changes relatively to the viewports width/height
2. **Vmin**: Size changes relatively to the smaller of the viewport&#39;s dimensions (height or width)
3. **vmax**: Size changes relatively to the larger of the viewport's dimensions (height or width)
4. **%**: Size changes relatively to the parent's size
5. **Rem**: size changes relatively to the root element

## Post-session

- View the post-session [here](../../../wiki/[ENG3.0]-Adaptive-layouts)