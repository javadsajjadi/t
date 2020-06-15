# ئاپاچی
<!-- position: 1 -->

بلودیت هەوڵ دەدا بە شێوازی خۆکارانە پەیکەرسازی سیستەم ریک بخە، گەر کێشەت نییە لە قۆناغەکانی دامەزراندنم پێویست بە بەردەوامی لە قۆناگەکانی دیکە نییە.

ڕاژەی وێبی ئاپاچی سوود لە `.htaccess` فایل دەگرێت بۆ هەڵگرتنی پەیکەرسازییەکان، دەتوانن دووبارە بینووسن. فایلی  `.htaccess` ئەم حەشاردراوە لە ڕاژەکار.

- گەر ئێوە لە لقی ڕیشە دادەمەزرێنن دەبێ لە حاڵتی بۆچوون دەربێنن `RewriteBase /`.
- گەر ئێوە بلودیت لە ژێر لقێک دادەمەزرێنن دەبێ لە حاڵتی بۆچوون لاببن, بۆ نمونە, `bludit`,  uncomment بیگۆڕن بە `RewriteBase /` وەک`RewriteBase /bludit/`.

ئەمە نمونەیێکە لە شڕۆڤەی سەرەوە لە فایلی `.htaccess` .

```
AddDefaultCharset UTF-8

<IfModule mod_rewrite.c>

# Enable rewrite rules
RewriteEngine on

# Base directory
#RewriteBase /

# Deny direct access to the next directories
RewriteRule ^bl-content/(databases|workspaces|pages|tmp)/.*$ - [R=404,L]

# All URL process by index.php
RewriteCond %{REQUEST_FILENAME} !-f
RewriteRule ^(.*) index.php [PT,L]

</IfModule>
```