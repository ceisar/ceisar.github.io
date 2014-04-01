---
layout: post
title: "Ubuntu Levazımlık"
date: 2014-01-06 14:08:41 +0200
comments: true
categories: teknik
---


{% img http://radorecdn.bobiler.org/upload/all/162/tarak_ustura_kalem_cakmak_isvicre_162529479b.jpg %}


##Ubuntu Kullananlar İçin Bir Kaç İşe Yarar Komut

**=> Ubuntu'nun hangi versiyonda olduğunu öğrenmek için ;**

```
dpkg -s libgtk-3-0 | grep '^Version'
```
<!--more-->

**=> Ubuntu komut satırı kullananlar için önem arz eden Guake (F12 kullanımlı)**
```
sudo apt-get install guake
```
*Kurulumdan sonra Alt + F2 'de guake yazın. Çalıştıktan sonra F12 tuşu ile Guake'i gökten zembille indirebilirsiniz.*

**=> DNS ayarlarını değiştirmek için ;**
```
sudo gedit /etc/resolv.conf
```
*şifrenizi girin ve ardından gelen sayfada* 
>nameserver 127.0.1.1

*yerine*

>nameserver 8.8.8.8

>nameserver 8.8.4.4

*yazıp kaydedin ve çıkın. Google DNS adresini örnek olarak verdim. Siz kefinize göre değiştirin.*

**=> Ubuntu'da sürekli root olmak için ;**

```
sudo su
```

**=> Ubuntu'da sürücü isimlerini görüntülemek için ;**

```
lspci
```

*Sadece ekran kartı sürücüsünün ismini görüntülemek için (örnek olarak ekran kartı) ;*

```
lspci | grep VGA
```

**=> Komut satırında "Mysql" kullanmak için ;**

```
mysql -u root -p
```

**=> Bilgisayarda ki bütün gizli dosyaları görüntülemek için ;**

```
find ~ - type f | ls -a | grep .*
```

*veya*

```
find - ~ - type f .*
```

**=> çalıştırılabilir dosyaları görüntüleyebilmek için gerekli komut ;**

*(Bu komut satırına `man find` yazdıktan sonra gelen sayfa içerisinde ve görüntülenen gizli dosyalar üzerinde denenmiştir.)*

```
find - ~ executable
```

![](http://image.hotdog.hu/user/Lancher/profil/tumblr_m6l5wzAwfC1qc3izto1_500.gif "Sherlock Holmes")