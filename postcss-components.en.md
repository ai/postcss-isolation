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
    top: 93px;
    right: 130px;
    width: 195px;
}
h2 {
    font-size: 52px;
    letter-spacing: 2px;
    position: relative;
    top: 15px;
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
    bottom: 50px;
}
&::after {
    visibility: hidden;
}
</style>

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

## [postcss-nested](https://github.com/postcss/postcss-nested)
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

## [autoprefixer](https://github.com/postcss/autoprefixer)
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
