<div dir="rtl">
  
#رێنمایی دامەزراندن
<!-- position: 3 -->

<h2 id="installation-from-zip-file">دامەزراندن لەرێگای پەڕگەی زیپ</h2>

1. داگرتنی دوایین وشان لەم ناونیشانە [پەڕەی فەرمی](https://www.bludit.com).
2. کردنەوەی پەڕگەی زیب.
3. بارکردنی فایلی کراوەی زیپ لە سەر ڕاژە یان ڕاژەکار. ئێوەدەتوانن لە لقی ڕیشەی ڕاژە باری بکەن, ئان لە ژێر لقێک بۆ وێنە `/bludit/`.
4. بۆ بارکردن لە ڕاژە دەتوانن لە, کلاینێتی FTP , WebFTP, یان ئەبزارەکانی دیکە کە کۆمپانیای ڕاژە دەیخەنە بەردەستان سوود بگرن.
4. سەردانی دۆمەینەکەتان بکەن. گەر ئێوە پەڕگەکان لە لقی ریشە بارتان کردووە بۆ وینە سەردانی ناونیشانی `https://www.example.com` بکەن, گەر لە ژێر لقی ریشە بارتان کردووە سەردانی `https://www.example.com/bludit/` بکەن.
5. شوێنی دامەزرێنەری بلودیت بۆ پەیکەرسازی ماڵپەڕەکەتان بکەوەن.
</div>

---

<div dir="rtl">
<h2 id="php-built-in-web-server"> لە ڕاژەکەتانPHP خزمەتگوزاری</h2>

ئێوە دەتوانن لە رێگای هێڵی فەرمان و  [PHP خزمەتگوزاری ڕاژەی](https://www.php.net/manual/en/features.commandline.webserver.php) بە خێرایی بلودیت جێبەجێبکەن.
</div>

```
$ git clone https://github.com/bludit/bludit.git
$ cd bludit
$ php -S localhost:8000
```

<div dir="rtl">
  
لە شریتی وێبگەرەکەتان بچنە نێو ئەم ناونیشانە `http://localhost:8000`
</div>

---

<div dir="rtl">
<h2 id="docker">دۆکێر</h2>
دامەزراندنی بلودیت لە رێگای [دۆکێر وێنەی فەرمی](https://hub.docker.com/r/bludit/docker/).

</div>

```
$ docker run --name bludit -p 8000:80 -d bludit/docker:latest
```
<div dir="rtl">
لە شریتی وێبگەرەکەتان بچنە نێو ئەم ناونیشانە `http://localhost:8000`
</div>

---

<div dir="rtl">
<h2 id="vagrant">Vagrant</h2>
دامەزراندنی وەیگرێنت لە  [دامەزراندنی فەرمی وەیگرێنت](https://pilab.dev/bludit-vagrant).
  
</div>

```
$ git clone https://github.com/mhancoc7/Bludit-Vagrant.git
$ cd Bludit-Vagrant
$ vagrant up
```

<div dir="rtl">
لە شریتی وێبگەرەکەتان بچنە نێو ئەم ناونیشانە `http://localhost:8080`
</div>

---

<div dir="rtl">
<div class="note">
<div class="title">ڕاژەی وێب</div>
دەتوانن لە بەستەرەکانی ڕووبەروو بۆ پەیکەرسازی ڕاژە هەوڵ بدەن. <a href="https://docs.bludit.com/en/webservers/apache">Apache</a> - <a href="https://docs.bludit.com/en/webservers/nginx">Nginx</a>
</div>
</div>
