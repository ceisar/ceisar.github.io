---
layout: post
title: "Sihirli Tuş 'SysRq'"
date: 2014-01-07 10:56:03 +0200
comments: true
categories: teknik
---

Ubuntu kullanırken bilgisayarımızda yavaşlama sıkıntısı yaşıyorsak eğer, bu tuş bize yardımcı oluyor. (Reset tuşuna bi son verin artık.) Klavyedeki yeri, sağ üst kısımlarda PrtSc (Print Screen) ile aynı tuşu paylaşıyor. Öncelikle SysRq tuşumuzun etkin olup olmadığını şu şu komutla belirliyoruz ;

```
cat /proc/sys/kernel/sysrq
```

<!--more-->

bu komutun çıktısı eğer `1` ise tuşumuz etkin demektir. Eğer değil ise, aşağıdaki komut ile, çıktımızı 1 olarak değiştiriyoruz.

```
sudo echo "1" > /proc/sys/karnel/sysrq
```
####Şimdi de nasıl kullanacağımıza bakalım.

`Alt + SysRq + komut_tuşu**`

Örnek olarak verirsek ;

`Alt + SysRq + r`

####Komut Tuşlarımız (**);

**r ==> Klavye X sunucusundan alır, çekirdek kontrolünde ham klavye kipine çevirir.**

**e ==> 'Nezaketen' bütün uygulamalara sonlandırma sinyali verir.**

**i ==> Tüm uygulamalara 'Nezaketen Olmayan' bir şekilde kapatma emri verir. Yani kill sinyali gönderir.**

**s ==> Ön belleği diske aktarır.**

**u ==> Tüm dosya sistemlerini salt-okunur olarak yeniden bağlar.**

**b ==> Bilgisayarı kontrollü bir biçimde (resetlemekten çok daha güvenli olarak) yeniden başlatır.**