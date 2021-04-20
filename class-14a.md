# CSS Transforms, Transitions, and Animations

## Transforms
ways to control size, position and change elements.

- The transform property coild be one of two different settings:
  - two-dimensional 
  - three-dimensional.

**Transform Syntax**
```````````````
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```````````````

**2D Transforms**

- Work in horizontal and vertical axes plane.

 *2D Rotate*
- ability to rotate element from 0 to 360 degrees.  
- positive value clockwise and negativr value rotate counterclockwise.

 *2D Scale*
- change the appeared size of an element.
- any `>1value>0`  makes element appera smaller,`value>=1` makes element appear larger.
- scale x to scale width and scale y to scale height.

*2D Translate*
- Pushing and pulling element in different directions.
- translateX change the horizontal position and translateY change the vertical position

*2D Skew*
- Used to distort elements on the horizontal axis vertical axis or both.

- Sometimes we combining multiple transforms for the same elements.
-  the default transform origin is the dead center of element both 50% horizontally and 50% vertically, to change default origin position we used the transform-origin property.
- The perspective property used to give a 3D-positioned element some perspective,  it defines how far the object is away from the user


**3D Transforms**

- Three-dimensional transforms work on both the x and y axes, as well as the z axis,  control of depth, length and width.

*3D Rotate*
- rotate element around any axis

*3D Scale*
- scaled on the z axis.

*3D Translate*
- Push the element away (appear smaller) or puul it closer (appera larger)

*3D Skew*
- elements can't be skewed on z-axis.

- We can combine 3D transforms as we can do with 2D too.
- three-dimensional transforms will be applied on element that is nested within a parent element.
- The back face of an element is a mirror image of the front face being displayed.


## Transitions & Animations

**Ttansitions**
- CSS transitions allows you to change property values smoothly, over a given duration when state change to active.

- different states is by using the :hover, :focus, :active, and :target pseudo-classes.

- four transition related properties:
    - transition-property (colors, font, boreder, ..etc)
    - transition-duration (s or ms)
    - transition-timing-function: speed in which a transition will move (linear, ease-in, ease-out, and ease-in-out.)
    -transition-delay: how long a transition should be stalled before executing
```````````````
.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}
```````````````

**Animation**

- CSS animation lets element gradually change from style to another.

- first we need to specify some keyframes for the animation.

- The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

- Animation name too assigned to an element.

- Animations behave similarly to transitions. They include a duration, timing function and delay if desired. 

- To have an animation repeat itself many times use the animation-iteration-count property.

- To declare the direction an animation completes use the animation-direction property.

- The animation-play-state property allows animation to be played or paused.

- The animation-fill-mode property identifies how element should be styled. 

- The animation-fill-mode property accepts four keyword values, including 
    - none: not apply any styles
    - forwards: keep the styles declared within the last specified keyframe.
    - backwards: apply the styles within the first specified keyfram
    - both: apply the behaviors from both the forwards and backwards values.

## 8 simple CSS Trasitions Examples

1. Fade in: by control capacity
2. Change color
3. Grow & Shrink by control width and height
4. Rotate elements
5. Square to circle by control the radius
6. 3D shadow
7. Swing by using @keyframes, animation 
8. Inset border









**Refrences:**
- [Transforms](https://learn.shayhowe.com/advanced-html-css/css-transforms/)
- [Transitions and Animations](https://learn.shayhowe.com/advanced-html-css/transitions-animations/)


