---
layout: post
title: "Ubuntu'ya 'Eclipse' Kurma"
date: 2014-01-07 12:15:16 +0200
comments: true
categories: teknik
---

##Eclipse'i kurmadan önce JDK'yı  kurmak gerekiyor.

`http://www.oracle.com/technetwork/java/javase/downloads/index.html`
adresinden JDK / JRE 'nin en güncel verisyonunu indirin.
İndirme işlemi bittikten sonra ;

```
cd İndirilenler		//veya sizin indirme dizininiz (ingilizce kullananlar için *'Downloads') 
```

<!--more-->

diyerek İndirilenler dizinine girin. Daha sonra indirmiş olduğumuz dosyayı çıkarmamız gerekiyor. Komut satırımıza aşağıdaki komutu yazıyoruz.

```
sudo tar -zxvf dosya_adi(*) -C/opt/
```

(*)dosya_adi = indirdiğin dosya versiyonuna göre değiştiği için ;

`jdk-7u4-linux-i586.tar.gz` gibi bir şey olabilir.

Yani örnek olarak komut satırına yazmanız gereken şey ;

```
sudo tar -zxvf jdk-7u4-linux-i586.tar.gz -C/opt/
```

şeklinde olmalı. Bunu yapınca dosyalar çıkarılırken aynı zamanda kendiliğinden bilgisayarımıza kurulmuş ta oldu. Kullanabilmek için ise PATH ayarlarının yapılması gerekiyor.

Bilgisayarımızı kapatıp açıyoruz ve daha sonra komut satırımıza ;

```
java -version
```

yazarak javamızınn hangi versiyonda olduğunu öğreniyoruz. Aynı zamanda bu komu bize yüklemenin doğru olduğunu/yapıldığını gösteriyor. Daha sonra komut satırına;

```
sudo gedit /etc/enviroment
```

yazıyoruz ve gelen dosyaya, `/opt/versiyonumuzun_adi(*)/bin` yazıyoruz. (*)versiyonumzun_adi kısmına kendi versiyonumuzu yazıyoruz. Yani örnek olarak `/opt/jdk1.7.0_04/bin` şeklinde yazmamız gerekiyor. Daha sonra bu dosyayı kaydedip çıkıyoruz.

Son olarak java'yı browserımızda kullanabilmek için, aşağıda ki kodu çalıştırarak pulgini browserımıza tanıtmış oluyoruz. (Chrome veya chromium için de geçerli mi bilmiyorum.)

```
sudo ln -s /opt/versiyonumuzun_adi(*)/jre/lib/i386/libnpjp2.so /usr/lib/mozilla/pulgins/
```

##Şimdi ise Eclipse kurulum evresine geçiyoruz.

`eclipse.org/downloads/` adresinden gerekli dosyayı (uzantısı .tar.gz olsun) indirin.

```
cd İndirilenler
```

Daha sonra yine indirdiğimiz dosyanın adını alıyoruz ve komut satırına ;

```
sudo tar -zxvf dosya_adi(*) -C/opt/
```

yazarak dosyayı çıkarıp aynı anda kurmuş oluyoruz.

Kurma işlemimiz tamamlandı.

Arama çubuğuna eclipse yazarak programı çalıştırabilirsin.

TEŞEKKÜRLER...