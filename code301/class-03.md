# Read : 03

## Flexbox and Templating

- Before the **Flexbox Layout module**, there were four layout modes:
  - Block, for sections in a webpage
  - Inline, for text
  - Table, for two-dimensional table data
  - Positioned, for explicit position of an element

- The **Flexible Box Layout Module**, makes it easier to design flexible responsive layout structure without using *float* or *positioning*.

- To start using the Flexbox model, you need to first define a flex container.

```
 <div class="flex-container">
  <div>1</div>
  <div>2</div>
  <div>3</div>
</div> 
```

- The flex container becomes flexible by setting the display property to flex:

```
.flex-container {
  display: flex;
}
```

- The flex container properties are:
    - flex-direction
    - flex-wrap
    - flex-flow
    - justify-content
    - align-items
    - align-content

- The flex item properties are:
    - order
    - flex-grow
    - flex-shrink
    - flex-basis
    - flex
    - align-self



##### [Go Back](code_301_reading_notes.md)