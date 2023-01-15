# Some Advanced CSS Theory

## Animations Note:

Sometomes animation can be shaking, to void that shaking effect use

```css
backface-visibility: hidden;
```

---

## Complex Animation

### pseudo-class

A pseudo-class is used to define a special state of an element.

- Style an element when a user mouses over it
- Style visited and unvisited links differently
- Style an element when it gets focus

---

## Three Pillars of HTML & CSS

### Responsive Design

- Fluid Layouts
- Media Queries
- Responsive Images
- Correct Units
- Desktop-first vs Mobile-first

### Maintainable and Scalable Code

- Clean & Easy to Understand
- Reusable
- How to organize files
- How to name classes
- How to structure HTML

### Web Performance

- Less HTTP requests
- Less code
- Compress code
- Use a CSS Predeccesor
- Less Images
- Compress Images

## Cascade & Specificity: What you need to know

- CSS declarations marked with `!important` have the highest priority.
- But onlu use `!important ` as a last resource, Its better to use an correct specificites - more mainatainable code.
- Inline styles will always have priority over styles in external stylessheets.
- A selector that contains 1 ID is more specific than one with 1000 classes.
- A Selector that contains 1 class is more specifc than one with 1000 elements
- The Universal Selector **`*`** has no specificity value(0,0,0,0)
- Rely more on **specificity** than on the **order** of the selctors.
- But rely on order when using 3rd party stylesheets- always put your author stylesheet last.

## CSS Value Processing

- Each property has an initial value, used if nothing is declared and if there is no inheritance
- Browsers specify a **root font-size** for each page(usually 16px).
- Percentages and relative value are always connected to pixels.
- Percentages are measured relative to their parent's **font size**, if used to specify font size.
- Percentages are measured relative to their parnent's **width**, if used to specify lengths.
- em are measured relative to their **parent** font size, if used to specify font-size.
- em are measured relative to their **current** font size, if used to specify lengths.
- rem are always measured relative to the **document root** font size.
- vh and vw are simply percentage measurements of the viewport's height and width.

## Inheritance

- Inheritance passes the values for some specific properties from parents and children- **more maintainable code**.
- Proprties related to text are inherited: font-family, font-size, color,etc.
- The Computed value of a property is what gets inherited, not the declared value.
- Inheritance of a property only works if no one declares a value for that property.
- The _inherit_ keyword forces inheritance on a certain property.
- The _initial_ keyword resets a value to its inital value.

---

## Installing SCSS

- Requirements : NodeJs

Run below command in terminal which will create package.json

```
npm init -y
```

Install `node-sass` as dev Dependcies

```
npm i -D node-sass
```

---

## Basic Resposnive Design Principles

1. FLUID LAYOUTS

- To allow webpage to adapt to the current viewport width(or even height).
- Use % (or vh/ vw) unit instead of px for elements that should adapt to viewport (usually layout).
- Use max-width instead of width

2. RESPONSIVE UNITS

- Use rem unit instead of px for most lengths
- To make it easy to scale the entire layout down(or up) automatically.

3. FLEXIBLE IMAGES
   -By default, images dont scale automatically as we change the viewport, so we need to fix that.

- Always use % for image dimensions, toghether with max-width property.

4. MEDIA QUERIES

- To change CSS styles on certain viewport widths(called breakpoints)

### LAYOUT TYPES

- Float Layouts : Old way of building layouts
- Flexbox: Modern way of layoing out elements in a 1-dimensional row without using float.Perfect for component layouts.
- CSS Grids: For laying out element in a fully fledged 2-dimensional grid. Perfect for page layout and component layouts.
