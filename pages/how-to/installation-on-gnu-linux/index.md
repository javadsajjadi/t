<div dir="rtl">

# دامەزراندن لە گنو/لینوکس
<!-- position: 3 -->

<h2 id="ubuntu">دامەزراندن لە سەر ئوبونتوی ١٦.٠٦ جێگیر</h2>

ڕچاوگرتن:
- PHP وشانی ٧.٠,بۆت هەیە لە وشانی دامەزراندنی ئێوە جیواز بێت، دەتوانن بەڕۆژی بکەن.
- PHP-FPM لە ژێر جێبەجیکردنی ناویبەکارهێنەر لەم مەسیرە `www-data`.
- PHP-FPM ئامادە لە سوکێتی دەرگای لینوکس لە م مەسیرە `unix:/run/php/php7.0-fpm.sock`.
- Nginx چالاک لەم مەسیرە `www-data`.
- پێویست بە دامەزراندنی هیچ خزمەتگوزاریێکی ڕاژە ناکەن.
- لە پەیکەرسازی بنەمایی، کەمێ خوێندن زیاد بکەن لەم بوارە بۆ دامەزراندنی هاسان تر

دامەزراندنی ڕاژەی Nginx , PHP, کەمێ ئامراز
</div>

```
$ sudo apt install -y nginx php-fpm php-dom php-mbstring php-cli php-gd php-opcache unzip
```
<div dir="rtl">
پەیکەرسازی Nginx.
</div>

```
$ sudo rm -f /etc/nginx/sites-enabled/*
```

<div dir="rtl">
دامەزراندنی پەڕگەیێک لە ڕاژەی خەیاڵێ لەم شوێنە `/etc/nginx/conf.d/bludit.conf`.
</div>

```
server {
	listen 80;
	server_name _;
	root /www/bludit;
	index index.php;

	location ~ \.php$ {
		fastcgi_pass    unix:/run/php/php7.0-fpm.sock;
		include         fastcgi.conf;
	}

	location / {
		try_files $uri $uri/ /index.php?$args;
	}
}
```

<div dir="rtl">
داگرتنی دوایین وشانی بلوو دیت بەم شێوازە
</div>

```
$ mkdir /www
$ cd /www
$ curl https://www.bludit.com/releases/bludit-latest.zip --output bludit-latest.zip
$ unzip bludit-latest.zip
$ sudo chown -R www-data:www-data /www
```

<div dir="rtl">
نوێکردنی خزمەتگوزارییەکان بۆ بارکردنی نوێی پەیکەرسازییەکان
</div>

```
$ sudo service php7.0-fpm restart
$ sudo service nginx restart
```
<div dir="rtl">
کردنەوەی وێبگەر و نووسینی ئەم ناونیشانە http://localhost بۆ ئەنجام دانی دامەزراندنی تەواو

<h2 id="centos">دامەزراندن لە  Centos 7 / Red Hat 7</h2>

Considerations:
- PHP-FPM لە حاڵێ جێبەجیکردن بێ لە ژێر ناوی `nginx`.
- PHP-FPM لە سوکێتی لینوکس لە حاڵێ جێبەجێبوون `unix:/run/php/php-fpm.sock`.
- Nginx لە حاڵێ جێبەجێکردن بێ لە ژێر ناوی `nginx`.
- پێویست بە دامەزراندنی هیچ خزمەتگوزاریێکی ڕاژە ناکەن.
- لە پەیکەرسازی بنەمایی، کەمێ خوێندن زیاد بکەن لەم بوارە بۆ دامەزراندنی هاسان تر

دامەزراندنی کانگای EPEL 
</div>

```
$ sudo yum install -y epel-release
```
<div dir="rtl">
دامەزراندنی خزمەتگوزاری ڕاژەی Nginx , PHP, بەشێک لە ئامرازەکانی دیکە
</div>

```
$ yum install -y nginx php-fpm php-cli php-dom php-mbstring php-zip php-gd
```
<div dir="rtl">
پەیکەرسازی Nginx, زیادکردنی پەڕگەیێک لە نێو بلۆک بەم شوێنە `/etc/nginx/conf.d/bludit.conf`.
</div>

```
server {
	listen 80;
	server_name _;
	root /www/bludit;
	index index.php;

	location ~ \.php$ {
		fastcgi_pass    unix:/run/php/php7.0-fpm.sock;
		include         fastcgi.conf;
	}

	location / {
		try_files $uri $uri/ /index.php?$args;
	}
}
```
<div dir="rtl">
دامەزراندنی دوایین وشانی بلوودیت
</div>

```
$ mkdir /www
$ cd /www
$ curl https://www.bludit.com/releases/bludit-latest.zip --output bludit-latest.zip
$ unzip bludit-latest.zip
$ sudo chown -R nginx:nginx /www
```
<div dir="rtl">
نوێکردنی خزمەتگوزارییەکان بۆ بارکردنی نوێی پەیکەرسازییەکان
</div>

```
$ sudo systemctl php-fpm restart
$ sudo systemctl nginx restart
```
<div dir="rtl">
کردنەوەی وێبگەر و نووسینی ئەم ناونیشانە http://localhost بۆ ئەنجام دانی دامەزراندنی تەواو
</div>
