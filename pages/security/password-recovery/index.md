<div dir="rtl">

# گەڕانەوەی تێپەڕوشە
<!-- position: 4 -->

ئێوە دەتوانن تێپەڕ وشە یان وشەی نهێنی   `admin` بە یارمەتی پەڕگەسکریپتی `recovery.php` بهێننەوە.

<h2 id="how-to-recover-the-password">جۆن تێپەڕوشە بهێنینەوە</h2>

1. پەڕگەی [recovery.php](https://raw.githubusercontent.com/bludit/password-recovery-tool/master/recovery.php) دابگرن
2.پەڕگەی `recovery.php` لە شوێنی دامەزراندنی بلودیت لە ریشە یان رەگی ڕاژە بار بکەن.
3. بەیارمەتی وێبگەڕەکەت ئەم پەڕگە بکەرەوە ، بۆ وێنە:: https://example.com/recovery.php, ناونیشانی ماڵپەڕەکەت بە جیاتی `example.com` بنووسن.
4. تێپەڕوشەی نهێنی بۆ بەکارهێنەری `admin` دروست وە لە وێبگەڕەکەت نیشان دەدرێت.
5. بە هەژمارەی بەکارهێنەری `admin` تێپەڕوشەی نوێ بچنەژووری بەڕێوەبەر.

سکریپتی recovery.php هەوڵ دەدا خۆی بسڕێتەوە، بەڵام گەر ئەم کردارە  خۆکارانە ئەنجام نەبوو، پێشنیار دەکەم بەدەستی لە ڕاژە بیسڕنەوە.

---

<h2 id="how-to-recover-the-password-via-command-line">بە هێڵێ فەرمان چۆن تێپەڕوشە بگەڕێنیەوە</h2>

ئێوە دەتوانن سکریپتی `recovery.php` لە نێو هێڵی فەرمان جێبەجێ بکەن.
</div>

```
# بڕۆنە نێو ئەو لقە کە بلودیتان دامەزراندووە
cd /var/html/bludit

# سکریپتەکە دابگرن
curl -o recovery.php https://raw.githubusercontent.com/bludit/password-recovery-tool/master/recovery.php

# ئامرازەکە جێبەجێ بکەن
php recovery.php
```

```
Bludit Password Recovery Tool

Username: admin
New password: 00bef4566011d2015df2786dbd094003

>> The file recovery.php was deleted automatically for security reasons. <<
```
