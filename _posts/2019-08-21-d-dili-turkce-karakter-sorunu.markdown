---
layout: post
title: "d programlama dili türkçe karakter sorunu"
lang: tr
tags: ["d dili", "dlang", "dmd", "utf8", "chcp 65001"]
categories: ["tip&tricks"]
---
![d programming language logosu](/images/logo-dlang.png)

Yapmanız gereken tek şey kodunuz derlendikten sonra, kodu çalıştıracağınız konsola UTF8'e geçmesini söylemek.
Kullandığınız terminalinize `chcp 65001` yazmanız yeterli.

Ben Türkçe karakter sorununu[1]: http://ddili.org/forum/post/8;?unb666sess=9a2ae08df7910b8e29b123d8df22cd05 bu şekilde çözdüm.

<h3>D Dili Nedir</h3>

Vikipedi'ye göre:
> D programlama dili, C++ dilinden daha yüksek seviyede ve hedef alınan işletim sistemiyle donanımlara göre uygulama yazılmasını kolaylaştıran bir "sistem ve uygulama" dilidir. D, C gibi sistem programlama dili olmasına karşın birçok üst düzey dilden özellikler almış olan kod okunabilirliği yüksek bir dildir.

Bu arada D dilinden bahsedip Ali Çehreli üstadı anmadan olmaz kendisine bize sunduğu Türkçe kaynaklar için teşekkür ederim.