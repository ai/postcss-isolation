# Fix Global CSS with PostCSS
!favicon ./favicon.ico
!theme   ../showbox-ai
!lang    en

[Andrey Sitnik](http://sitnik.ru/en), [Evil Martians](https://evilmartians.com/)

<style>
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
    bottom: 35px;
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

## **1 300 000** Downloads per Month

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
    line-height: 1.7;
}
</style>

## Analog WhatsUp

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

## And then Global CSS :(

```css
* {
    box-sizing: border-box;
}
.title {
    font-size: 30px;
}
```
