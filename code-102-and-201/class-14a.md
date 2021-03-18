# CSS Transforms, Transitions, and Animations

### CSS Transforms

The transform property comes in two different settings, two-dimensional and three-dimensional. Each of these come with their own individual properties and values.
```css
transform: rotate(20deg);

transform: scale(.75);
transform: scaleX(.5);
transform: scaleY(1.15);
transform: scale(.5, 1.15);

transform: translateX(-10px);
transform: translateY(25%);
transform: translate(-10px, 25%);

transform: skewX(5deg);
transform: skewY(-20deg);
transform: skew(5deg, -20deg);
```
You can combine transforms:
```css
transform: rotate(25deg) scale(.75);
```

transform origin:

the default value is 50% 50% 'the center of the item'
```css     
transform-origin: 0 0;
```

#### 3D Transforms:

the same transforms for 2d except that you need to add the perspective value as shown:

```css
transform: perspective(200px) rotateY(45deg);
```

>Skew is the one two-dimensional transform that cannot be transformed on a three-dimensional scale. 


also check out these:
```css
transform-style: preserve-3d;
backface-visibility: hidden;
```


### Transition and Animations


Animations within CSS3 allow the appearance and behavior of an element to be altered in multiple keyframes. Transitions provide a change from one state to another, while animations can set multiple points of transition upon different keyframes.

```css
transition-property: background, border-radius;  transition-duration: 1s,2s;
transition-timing-function: linear; //linear, ease-in, ease-out, and ease-in-out.
transition-delay: 0s, 1s;
```

Shorthand Transitions:
```css
transition: background .2s linear, border-radius 1s ease-in 1s;
```

Transitions do a great job of building out visual interactions from one state to another, and are perfect for these kinds of single state changes. However, when more control is required, transitions need to have multiple states. In return, this is where animations pick up where transitions leave off.


To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.


>The @keyframes rule must be vendor prefixed

```css
@keyframes animate {
}

animation-name: animate;
animation-duration: 2s;
animation-timing-function: ease-in-out;
animation-delay: .5s;
animation-iteration-count: infinite;
animation-direction: alternate;
```

The `animation-play-state` property allows an animation to be played or paused using the running and paused keyword values respectively. When you play a paused animation, it will resume running from its current state rather than starting from the very beginning again.
```css
animation-play-state: paused;
```

also:
```css
animation-fill-mode: forwards;
```

Shorthand Animations;
```css
    animation: slide 2s ease-in-out .5s infinite alternate;
```
