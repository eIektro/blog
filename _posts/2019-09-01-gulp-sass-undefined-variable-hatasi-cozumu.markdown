---
layout: post
title: "Gulp sass/scss undefined variable hatası çözümü"
lang: tr
tags: ["gulp", "sass", "scss", "node", "front-end"]
categories: ["tip&tricks"]
---

<h3>Gulp-sass/scss compiler error: undefined variable</h3>

Bu compile hatasını alıyorsanız öncelikle sakın panik yapmayın :) Yapmanız gereken çok basit. 

`variable.sccs` şeklindeki dosya adını `_variable.scss` olarak düzenliyorsunuz. etkilenen dosyalarınızı da aynı şekilde başına alt çizgi (underscore) ekliyorsunuz. Ve `gulp watch` yazdığınızda.. Boom, çalışıyor :)