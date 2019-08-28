---
layout: post
title: "warning:LF will be replaced by CRLF çözümü"
lang: tr
tags: ["git", "lf", "crlf", "satır sonu", "end of line squence"]
categories: ["tip&tricks"]
---

Kısaca bu uyarının temel nedeni şudur. Herhangi bir işletim sisteminde editörde bir yazı yazarken "Enter"layıp bir alt satıra geçtiğinizde OS satırın bittiğini bildirmek için -görmeyeceğiniz- bir işaret koyar ve sizi alt satıra geçirir. 
Linux'te ve Windows'ta veya herhangi bir işletim siteminde bu gizli işaretin farklı olması bu sorunu ortaya çıkarır.


<h2>warning:LF will be replaced by CRLF in git çözümü</h2>

Bu uyarı çıkmadan satır sonları otomatik olarak CRLF çevrilsin istiyorsak. Git Bash'te aşağıdaki komutu yazabiliriz.

```git
git config --global core.autocrlf true
```

Herhangi bir dönüşüme ihtiyacınız yoksa değeri false yapabilirsiniz.

```git
git config --global core.autocrlf false
```