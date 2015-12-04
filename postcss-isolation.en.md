# Fix Global CSS with PostCSS
!favicon ./favicon.ico
!theme   ../showbox-ai
!lang    en

[Andrey Sitnik](http://sitnik.ru/en), [Evil Martians](https://evilmartians.com/)

<style>
.slide.cover h2 {
    color: white;
    font-family: "Open Sans";
}
.slide.with-shadow h2 {
    text-shadow: 1px  1px 1px black, -1px  1px 1px black,
                 1px -1px 1px black, -1px -1px 1px black;
}
.slide.is-yellow h2 {
    color: black;
    text-shadow: 1px  1px 1px #f6ef85, -1px  1px 1px #f6ef85,
                 1px -1px 1px #f6ef85, -1px -1px 1px #f6ef85;
}
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
!cover what.jpg

<style>
h2 {
    position: absolute;
    bottom: 60px;
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
    <div class="line" style="height: 115.56%"></div>
    <div class="line" style="height: 140.56%"></div>
</div>

<style>
.stat {
    margin-top: 50px;
    height: 245px;
    position: relative;
    font-size: 0;
}
.line {
    display: inline-block;
    background: #0080e0;
    width: 30px;
    margin-left: 4px;
    &:first-child {
        margin-left: 0;
    }
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
!cover problem.jpg
!type  with-shadow

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

## Why did we create computers?
!cover war.jpg
!type  with-shadow

<style>
h2 {
    position: absolute;
    bottom: 60px;
}
</style>

## 1. All machines **must suffer**
!cover suffer.jpg
!type  with-shadow

<style>
h2 {
    text-align: right;
    padding-left: 400px;
    line-height: 1.4;
}
</style>

## 2. Divide and Conquer
!cover parts.jpg

<style>
h2 {
    color: black;
}
</style>

## OSI/ISO

<table>
<tbody>

<tr style="background:#d8ec9b;">
<td>7.&nbsp;Application</td>
<td>HTTP, FTP, SMTP, SSH, TELNET</td>
</tr>

<tr style="background:#d8ec9b;">
<td>6.&nbsp;Presentation</td>
<td>HTML, CSS, GIF</td>
</tr>

<tr style="background:#d8ec9b;">
<td>5. Session</td>
<td>RPC, PAP, SSL, SQL</td>
</tr>

<tr style="background:#e7ed9c;">
<td>4. Transport</td>
<td>TCP, UDP, NETBEUI</td>
</tr>

<tr style="background:#eddc9c;">
<td>3. Network</td>
<td>IPv4, IPv6, IPsec, AppleTalk, ICMP</td>
</tr>

<tr style="background:#e9c189;">
<td>2. Data link</td>
<td>PPP, IEEE 802.2, L2TP, MAC, LLDP</td>
</tr>

<tr style="background:#e9988a;">
<td>1. Physical</td>
<td>Ethernet physical layer, DSL, USB, ISDN, DOCSIS</td>
</tr>

</tbody></table>

<style>
table td {
    background: none;
    border: 2px solid white;
    border-width: 2px 0;
    padding: 0 15px;
    &:first-child {
        font-weight: bold;
    }
}
</style>

## Operating System

!image systemd.svg

## CommonJS

```js
var React = ***require***('react');

module.***exports*** = React.createClass({
    …
});
```

## Design Style Guides

!image material.jpg

<style>
img {
    position: relative;
    top: -20px;
    display: block;
    width: 500px;
    margin: 0 auto;
}
</style>

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
!cover solution.jpg

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
!cover light.jpg
!type  is-yellow

<style>
h2 {
    position: absolute;
    bottom: 60px;
}
</style>

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
!cover broke.jpg
!type  is-yellow

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
!cover carry.jpg
!type  with-shadow

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

## [postcss-cssnext](https://github.com/cssnext/postcss-cssnext)
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
!cover alien.jpg
!type  with-shadow

## Problem

```css
/* Page width */
@media ***(max-width: 600px)*** {
    .photo {
        width: auto;
    }
}
```

## Component Media Queries

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

## *Part 8* Summary
!cover walking.jpg
!type  with-shadow

## Absolute Isolation with PostCSS

1. Transformations: `postcss-use`
2. Selectors: `postcss-modules`
3. Reset: `postcss-autoreset`
4. Properties: `all: inital` and `postcss-cssnext`
5. Media Queries: `cq-prolyfill`

## PostCSS is not an Enemy of Sass
!type with-2-sides

**Legacy project:**

**New project:**

```js
.pipe( ***sass***() )
.pipe( postcss([
    ...plugins
]) )
```

```js
.pipe( postcss([
    ***precss***,
    ...plugins
]) )
```

## <a class="github" href="http://github.com/postcss/postcss">github.com/<strong>postcss</strong>/<strong>postcss</strong></a>

* Twitter: [@postcss](https://twitter.com/postcss)
* Me: [@andreysitnik](https://twitter.com/andreysitnik)
* Blog: [@evilmartians](https://twitter.com/evilmartians)
* Evil Martians: [evl.ms](https://evilmartians.com/)

!image martians.svg

<style>
a {
    background: none;
}
h2 a {
    color: gray;
    font-family: Open Sans, sans-serif;
}
h2 strong {
    padding: 0 10px;
    color: black;
}
&::after {
    visibility: hidden;
}
ul {
    position: relative;
    top: 10px;
}
li {
    font-size: 180%;
    line-height: 1;
    padding-bottom: 40px;
    &::before {
        visibility: hidden;
    }
    &:first-child {
        margin-top: 90px;
    }
}
img {
    position: absolute;
    bottom: 105px;
    right: 100px;
    width: 320px;
}
</style>
