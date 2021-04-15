# Square loader

This loader is dependent of the root font size (rem).  
If `1rem` is equal to `16px` the loader is `60px` x `60px` (ie the default in most browsers.)

## Usage

Copy and paste the following snippet in your **HTML** markup:

```
<div class="square">
  <div></div>
  <div></div>
  <div></div>
  <div></div>
</div>
```

Copy and paste the following code-block in your **CSS** file:

```
.square {
  position: relative;
  height: 3.75em;
  width: 3.75em;
}
.square div {
  height: 100%;
  width: 100%;
  position: absolute;
  animation-duration: 0.4s;
  animation-timing-function: linear;
  animation-iteration-count: infinite;
}
.square div:nth-child(odd) {
  animation-name: topBottom;
  animation-delay: 0.2s;
}
.square div:nth-child(even) {
  animation-name: rightLeft;
}
.square div:nth-child(1) {
  border-top: 0.2em solid #ff0000;
  top: 0;
  left: 0;
}
.square div:nth-child(2) {
  border-right: 0.2em solid #ff0000;
  top: 0;
  right: 0;
}
.square div:nth-child(3) {
  border-bottom: 0.2em solid #ff0000;
  right: 0;
  bottom: 0;
}
.square div:nth-child(4) {
  border-left: 0.2em solid #ff0000;
  left: 0;
  bottom: 0;
}

@keyframes topBottom {
  0% {
    width: 0;
  }
  75% {
    width: 100%;
    opacity: 1;
  }
  100% {
    width: 100%;
    opacity: 0;
  }
}
@keyframes rightLeft {
  0% {
    height: 0;
  }
  75% {
    height: 100%;
    opacity: 1;
  }
  100% {
    height: 100%;
    opacity: 0;
  }
}
```

### Even easier if you use Sass!

Copy and paste the following code-block in your **SCSS** file:

```
$border: 0.2em solid #ff0000;

.square {
  position: relative;
  height: 3.75em;
  width: 3.75em;

  div {
    height: 100%;
    width: 100%;
    position: absolute;
    animation-duration: 0.4s;
    animation-timing-function: linear;
    animation-iteration-count: infinite;
  }

  div:nth-child(odd) {
    animation-name: topBottom;
    animation-delay: 0.2s;
  }

  div:nth-child(even) {
    animation-name: rightLeft;
  }

  div:nth-child(1) {
    border-top: $border;
    top: 0;
    left: 0;
  }
  div:nth-child(2) {
    border-right: $border;
    top: 0;
    right: 0;
  }
  div:nth-child(3) {
    border-bottom: $border;
    right: 0;
    bottom: 0;
  }
  div:nth-child(4) {
    border-left: $border;
    left: 0;
    bottom: 0;
  }
}

@keyframes topBottom {
  0% {
    width: 0;
  }
  75% {
    width: 100%;
    opacity: 1;
  }
  100% {
    width: 100%;
    opacity: 0;
  }
}

@keyframes rightLeft {
  0% {
    height: 0;
  }
  75% {
    height: 100%;
    opacity: 1;
  }
  100% {
    height: 100%;
    opacity: 0;
  }
}
```

[Online DEMO](https://microlab.se/square-loader/)
