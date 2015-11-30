# Fix Global CSS with PostCSS
!favicon ./favicon.ico
!theme   ../showbox-ai
!lang    en

[Andrey Sitnik](http://sitnik.ru/en), [Evil Martians](https://evilmartians.com/)

<style>
.slide.shout h2 {
    line-height: 1.6;
}
.slide.with-2-sides {
    pre, p, ul, ol {
        float: left;
        clear: left;
        width: 350px;
        &:nth-of-type(2) {
            float: right;
            clear: right;
        }
    }
}
</style>

## Fix Global CSS with **PostCSS**

!image postcss.svg

Andrey Sitnik, Evil Martians

<style>
img {
    position: absolute;
    top: 78px;
    right: 130px;
    width: 195px;
}
h2 {
    font-size: 52px;
    letter-spacing: 2px;
    position: relative;
}
h2 strong {
    display: block;
    font-size: 244%;
    margin: 15px 0 10px 0;
    position: relative;
    left: -6px;
}
p {
    font-family: "Open Sans Light";
    font-style: normal;
    position: absolute;
    bottom: 30px;
}
&::after {
    visibility: hidden;
}
</style>

## *Part 1* What is PostCSS?

## Inside PostCSS

<div class="postprocessing">
    <div class="step is-css">
        CSS
        <span class="position">
            <div class="note">source map</div>
        </span>
    </div>
    <div class="step is-important">Parser</div>
    <div class="step">Plugin</div>
    <div class="step">Plugin</div>
    <div class="step is-important">Stringifier</div>
    <div class="step is-css">
        New CSS
        <span class="position">
            <div class="note">new source map</div>
        </span>
    </div>
</div>

<style>
.postprocessing {
    position: relative;
    margin: 0 auto;
    width: 210px;
    top: -40px;
}
.step {
    height: 50px;
    line-height: 50px;
    border: 1px solid;
    text-align: center;
    position: relative;
    width: 100%;
    margin-top: 32px;
    margin-left: 3px;
    font-size: 115%;
}
.step:after {
    content: "↓";
    font-size: 70%;
    color: black;
    position: absolute;
    top: -46px;
    left: 97px;
}
.step:first-child {
    margin-top: 0;
}
.step:first-child:after {
    display: none;
}
.step.is-css {
    padding: 0;
    height: auto;
    line-height: 1.1;
    border: none;
}
.step.is-css:after {
    top: -27px;
}
.step.is-important {
    padding: 0;
    color: #0080e0;
    border-width: 4px;
    margin-left: 0;
    font-weight: bold;
}
.step.is-important:after {
    top: -48px;
}
.position {
    position: relative;
}
.note {
    position: absolute;
    top: 11px;
    left: 15px;
    font-size: 55%;
    white-space: nowrap;
}
</style>

## *Plugin Example* [postcss-nested](https://github.com/postcss/postcss-nested)
!type with-2-sides

```css
.block {
    ***&_title*** {
        font-size: 200%;
    }
}
```

```js
***.block_title*** {
    font-size: 200%;
}
```

## *Plugin Example* [autoprefixer](https://github.com/postcss/autoprefixer)
!type with-2-sides

```css
:fullscreen {
}
```

```css
:***-webkit-***full-screen {
}
:***-moz-***full-screen {
}
:***-ms-***fullscreen {
}
:fullscreen {
}
```

## **1 200 000** Downloads per Month

<div class="stat">
    <div class="line" style="height: 0.67%"></div>
    <div class="line" style="height: 1.11%"></div>
    <div class="line" style="height: 2.56%"></div>
    <div class="line" style="height: 4.3%"></div>
    <div class="line" style="height: 5.41%"></div>
    <div class="line" style="height: 9.22%"></div>
    <div class="line" style="height: 13.1%"></div>
    <div class="line" style="height: 15.94%"></div>
    <div class="line" style="height: 20.56%"></div>
    <div class="line" style="height: 24.85%"></div>
    <div class="line" style="height: 27.34%"></div>
    <div class="line" style="height: 26.79%"></div>
    <div class="line" style="height: 33.45%"></div>
    <div class="line" style="height: 43.43%"></div>
    <div class="line" style="height: 48.81%"></div>
    <div class="line" style="height: 59.05%"></div>
    <div class="line" style="height: 71.5%"></div>
    <div class="line" style="height: 75.56%"></div>
    <div class="line" style="height: 89.25%"></div>
    <div class="line" style="height: 100%"></div>
    <div class="line" style="height: 121.14%"></div>
</div>

<style>
.stat {
    margin-top: 50px;
    height: 280px;
    position: relative;
}
.line {
    display: inline-block;
    background: #0080e0;
    width: 32px;
}
</style>

## PostCSS Users

<p>

!image google.svg
!image wordpress.svg
!image taobao.svg
!image webpack.png

</p>

<style>
p {
    padding-top: 5px;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}
img {
    position: relative;
    max-height: 90px;
    max-width: 320px;
    padding: 40px;
    &:nth-of-type(4) {
        top: -30px;
        max-height: 180px;
    }
}
</style>

## *Part 2* Problem

## Thinking Sass

```css
.foo {
    ***@mixin*** transition(width 1s);
    ***@mixin*** rtl-float(left);
}
```

## Use PostCSS to keep code maintainable—not just for syntax sugar
!type shout

<style>
h2 {
    font-size: 290%;
}
</style>

## All machines must suffer

## Divide and Conquer

## Modern Computer

## OSI/ISO

## CommonJS

```js
var React = ***require***('react');

module.***exports*** = React.createClass({
    …
});
```

## Design Styleguides

## And then Global CSS **:-(**

```css
* {
    box-sizing: border-box;
}
.title {
    font-size: 30px;
}
```

## Problems

1. Global selectors
2. Global reset
3. Inherited properties
4. Page based media queries

## *Part 3* Components

## Isolated Components

<ul>
    <li>
        <code>logo/</code>
        <ul>
            <li><code>logo.js</code></li>
            <li><code>logo.css</code></li>
            <li><code>logo.svg</code></li>
        </ul>
    </li>
    <li>
        <code>header/</code>
        <ul>
            <li><code>header.js</code></li>
            <li><code>header.css</code></li>
        </ul>
    </li>
</ul>

## [postcss-use](https://github.com/postcss/postcss-use)

```css
***@use*** postcss-center;

.logo {
    top: center;
}
```

## *Part 4* Selectors

## Problem
!type with-2-sides

```css
/* logo.css */
***.name*** {
    font-size: 20px;
}
```

```css
/* header.css */
***.name*** {
    font-size: 16px;
}
```

## [postcss-bem](https://github.com/ileri/postcss-bem)
!type with-2-sides

```css
***@b*** Logo {
    ***@e*** name {
        color: gray;
    }
}
```

```css
.***Logo***-name {
    color: gray
}
```

## All machines must suffer
!type shout

## [CSS Modules](https://github.com/css-modules/css-modules)
!type with-2-sides

```css
.name {
    color: gray;
}
```

```css
.***Logo***__name__***sVK0p*** {
    color: gray
}
```

## Client Side: [webpack](https://github.com/webpack/css-loader)

```js
import ***styles*** from './logo.css';

class Logo extends React.Component {
    render() {
        return <div className={ ***styles.name*** }></div>;
    }
}
```

## Server Side: [postcss-modules](https://github.com/outpunk/postcss-modules)

```js
- ***styles*** = read_json('components/logo/logo.css.json')

div( class=***styles['logo']*** )
  div( class=***styles['name']*** )
```

## *Part 5* Reset

## Problem

```css
*** * *** {
    box-sizing: border-box;
    padding: 0;
    margin: 0;
}
```

## [postcss-autoreset](https://github.com/maximkoretskiy/postcss-autoreset)
!type with-2-sides

```css
.logo {
}
.name {  
}
.name.is-big {
}
```

```css
.logo {
    all: ***initial***;
}
.name {
    all: ***initial***;
}
.name.is-big {
}
```

## Configuration

```js
autoreset({
    reset: {
        'box-sizing': 'border-box',
        'all': 'initial'
    }
});
```

## *Part 6* Properties

## Inherited Properties

```html
<Header>
    ***color: white***
    <Logo>
        ***background: white***
    </Logo>
</Header>
```

## Third-Party Widgets

```css
h2 {
    color: red;
}
div {
    margin-top: 10px;
}
```

## [postcss-cssnext](#todo)
!type with-2-sides

```css
.logo {
    all: initial;
}
```

```css
.logo {
    color: black;
    background: white;
    box-sizing: content-box;
    line-height: normal;
    text-shadow: none;
    vertical-align: baseline;
    white-space: normal;
```

## *Part 7* Media Queries

## Problem

```css
/* Page width */
@media ***(max-width: 600px)*** {
    .photo {
        width: auto;
    }
}
```

## Components Media Queries

```css
.photo***:container***(width <= 600px) {
    width: auto;
}
.photo***:container***(background-color lightness < 20%) {
    color: white;
}
```

## [cq-prolyfill](https://github.com/ausi/cq-prolyfill)

```html
<script src="***cq-prolyfill.min.js***" async></script>
```
