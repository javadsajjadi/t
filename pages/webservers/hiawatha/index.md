# Hiawatha
<!-- position: 3 -->

بلودیت پاڵپشتی لە ڕاژەکاری Hiawatha دەکا. بۆ بەهێزکردن دەبێ وەک هێڵەکانی خوارەوە پەیکەرسازی ئەنجام بدەن:

```
UrlToolkit {
    ToolkitID = bludit
    RequestURI exists Return
    Match [^?]*(\?.*)? Rewrite /index.php$1
}
```
