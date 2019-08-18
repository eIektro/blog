---
layout: post
title: "my.conf dosyası windows'ta nerede"
lang: tr
tags: [mysql, veritabanı, windows]
categories: [tip&tricks]
---
![bilmeyenler için mysql logosu](/images/logo-mysql.png)
Merhabalar, 
Herhangi bir web development kütüphanesi kullanarak Windows üzerinde iş yapmanız gerekiyor. Kullanacağınız git reposunu yerel dizininize çektiniz. localhost kurup, veritabanını bağlayıp başlayacaksınız. 

mysql'i indirdiniz next next diyip kurdunuz. kendinizce ayarlarını da yaptınız ve çektiğiniz repo'da -atıyorum proje django projesi olsun- `database config` yani veritabanının ayarlarının olduğu kısımda `/etc/mysql/my.cnf` gibi bir konum gözüküyor. 

Bu demek oluyor ki projeyi github, bitbucket, gitlab veya vs. konuma yükleyen arkadaş projeyi linux üzerinde geliştiriyor. o nedenle sizin bu kısımı Windows'taki karşılığı olan `my.ini` dosyasının konumu ile değiştirmeniz gerekiyor. Eğer dediğim gibi next next diyerek kurduysanız, o konum da şurası oluyor:

`C:\ProgramData\MySQL\MySQL Server\my.ini`

Not: İşi bilen bir yazılımcının bu tarz bir bilgiye ihtiyacı olduğunu sanmıyorum. laf olsun diye yazılmıştır. :)