# خزمەتگوزارییکەانی زانیاری ئینتەرنێت (IIS)
<!-- position: 4 -->

هەر چەند بلودیت بۆ ئەم ڕاژە دروست نەکراوە بەڵام بە پەیکەر سازییێکی چاک دەتوانن ڕاژەی وێبی IIS بۆ  [PHP](https://docs.microsoft.com/en-us/iis/application-frameworks/scenario-build-a-php-website-on-iis/configuring-step-1-install-iis-and-php) 5.6+دامەزرێنن   the WebExt بە ماژۆڵێ [URL Rewrite](https://www.iis.net/downloads/microsoft/url-rewrite) دوبارەنووسی بکەن.

سەرەتا پێویستان بە وەرگێڕانی فالی `.htaccess` ئینجا فایلەکە ناچار بە دووبارەنووسینی یاسا کان بکەنەوە لە فایلی`web.config` .

```
<?xml version="1.0" encoding="UTF-8"?>
<configuration>
    <system.webServer>
        <rewrite>
            <rules>
                <rule name="Rule1" stopProcessing="true">
                    <match url="^bl-content/x(.*)\.txt$" ignoreCase="false" />
                    <action type="Redirect" url="{R:0}" redirectType="Temporary" />
                </rule>
                <rule name="Rule2" stopProcessing="true">
                    <match url="^(.*)" ignoreCase="false" />
                    <conditions logicalGrouping="MatchAll">
                        <add input="{REQUEST_FILENAME}" matchType="IsFile" ignoreCase="false" negate="true" />
                    </conditions>
                    <action type="Rewrite" url="index.php" />
                </rule>
            </rules>
        </rewrite>
    </system.webServer>
</configuration>
```

دووهەم، پێویستمان بە دانانی هەژمارەی خزمەتگوزاری IIS (وەک`IUSR`) بۆ چاودێری تەواوی بوخچەکان لە `bl-content` هەیە.

هەموو شتیک دەبێ لە دەرەوەی بۆکس بێت.