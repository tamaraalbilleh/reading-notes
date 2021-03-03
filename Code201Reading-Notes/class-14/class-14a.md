# Transforms
The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.
## Transform Syntax
```
div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);
}
```
## 2D Transforms
Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes. Three-dimensional transforms work on both the x and y axes, as well as the z axis. 
## 2D Rotate
The rotate value provides the ability to rotate an element from 0 to 360 degrees.
## 2D Scale
Using the scale value within the transform property allows you to change the appeared size of an element.
## 2D Translate
Using the translateX value will change the position of an element on the horizontal axis while using the translateY value will change the position of an element on the vertical axis.
## 2D Skew
skew, is used to distort elements on the horizontal axis, vertical axis, or both
## 3D Transforms
### 3D Rotate
With three-dimensional transforms we can rotate an element around any axes. To do so, we use three new transform values, including rotateX, rotateY, and rotateZ.
### 3D Scale
By using the scaleZ three-dimensional transform elements may be scaled on the z axis.
### 3D Translate
Elements may also be translated on the z axis using the translateZ value. A negative value here will push an element further away on the z axis, resulting in a smaller element. Using a positive value will pull an element closer on the z axis, resulting in a larger element.
### 3D Skew
Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale
***
# Transitions & Animations
## Transitions
There are four transition related properties in total, including transition-property, transition-duration, transition-timing-function, and transition-delay
## Transitional Property
The transition-property property determines exactly what properties will be altered in conjunction with the other transitional properties.
It is important to note, not all properties may be transitioned, only properties that have an identifiable halfway point.
## Transition Duration
The duration in which a transition takes place is set using the transition-duration property.
As with the transition-property property value, multiple durations can be declared using comma separated values
## Transition Timing
The transition-timing-function property is used to set the speed in which a transition will move.
## Transition Delay
On top of declaring the transition property, duration, and timing function, you can also set a delay with the transition-delay property. The delay sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing.
##  Animations
### Animations Keyframes 
The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.
### Animation Name
Once the keyframes for an animation have been declared they need to be assigned to an element. To do so, the animation-name property is used with the animation name, identified from the @keyframes rule, as the property value.
### Animation Duration, Timing Function, & Delay
Once you have declared the animation-name property on an element, animations behave similarly to transitions. 
***
# 8 SIMPLE CSS3 TRANSITIONS THAT WILL WOW YOUR USERS
1. Fade in
2. Change color
3. Grow & Shrink
4. Rotate elements
5. Square to circle
6. 3D shadow
7. Swing
8. Inset border

