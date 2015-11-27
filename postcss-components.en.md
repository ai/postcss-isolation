# Fix Global CSS with PostCSS
!favicon ./favicon.ico
!theme   ../showbox-ai
!lang    en

[Andrey Sitnik](http://sitnik.ru/en), [Evil Martians](https://evilmartians.com/)

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
