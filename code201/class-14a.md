# Class 14 Reading Notes (Part 1)

## CSS Transforms, Transitions and Animations  


### Transform Property  

- The `transform` property applies a 2D or 3D transformation to an element.  

- This property allows you to rotate, scale, move, skew, etc., elements.  

- Some `transform` property values:
    - **none** : Defines that there should be no transformation.
    - **scale(x,y)** : Defines a 2D scale transformation.
    - **rotate(angle)** : Defines a 2D rotation, the angle is specified in the parameter.

- Example:
```
div.a {
  transform: rotate(20deg);
}
div.b {
  transform: skewY(20deg);
}
div.c {
  transform: scaleY(1.5);
}
```


### Transition Property  

- The `transition` property is a shorthand property for:
    - `transition-property` : Specifies the name of the CSS property the transition effect is for.
    - `transition-duration` : Specifies how many seconds or milliseconds the transition effect takes to complete.
    - `transition-timing-function` : Specifies the speed curve of the transition effect.
    - `transition-delay` : Defines when the transition effect will start.

- Example: Hover over a `<div>` element to gradually change the width from **100px** to **300px**:
```
div {
  width: 100px;
  transition: width 2s;
}
div:hover {
  width: 300px;
}
```


### Animation Property

- The `animation` property is a shorthand property for:
    - `animation-name` : Specifies the name of the keyframe you want to bind to the selector.
    - `animation-duration` : Specifies how many seconds or milliseconds an animation takes to complete.
    - `animation-timing-function` : Specifies the speed curve of the animation.
    - `animation-delay` : Specifies a delay before the animation will start.
    - `animation-iteration-count` : Specifies how many times an animation should be played.
    - `animation-direction` : Specifies whether or not the animation should play in reverse on alternate cycles.
    - `animation-fill-mode` : Specifies what values are applied by the animation outside the time it is executing.
    - `animation-play-state` : Specifies whether the animation is running or paused.

- Example: Binding an animation to a `<div>` element, using the shorthand property:
```
div {
  animation: mymove 5s infinite;
}
```


##### [Go Back](code_201_reading_notes.md)