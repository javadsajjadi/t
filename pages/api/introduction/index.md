<div dir="rtl">
  
  #  پێشەکی API
<!-- position: 1 -->

APIـی بلوودیت (ڕوخساری بەرنامەنووی نەرمەکالا) جۆرێک دیزاین کراوە کە بە سادەیی دەتوانێت تێكڵاو تواناییەکان بلوودیت کرێت. بەم زیادکراوە, زانیارییەکان بەڕۆژ یان دەستکاری بکەن بە داوای HTTP .

<h2 id="installation">دامەزراندن</h2>
زیادکراوەی API پە پێشەوە دامەزراوە  ئێوە تەنها دەبێ ئەم زیادکراوە چالاک بکەن
</div>

```bash
Admin panel > Plugins > API > Activate
```

<div dir="rtl">
<h2 id="url">URL</h2>
ناونیشانی API بەم جۆرەیە:
</div>

```bash
{protocol}://{domain}/api/{endpoint}
````

<div dir="rtl">
نمونە:
</div>

```bash
https://www.example.com/api/pages
```

<div dir="rtl">
<h2 id="endpoints">خاڵەکۆتاییەکانی مێتۆدەکان</h2>

| endpoint | method | description |
|----------|--------|-------------|
| /pages | `GET` | پێرستێک لە پەڕەکان دەگەرێنێتەوە |
| /pages/{page key} | `GET` | پەڕەیێک لە لایەن کلیلی پەڕەیێکی دی دەگەڕێنێتەوە |
| /pages | `POST` | پەڕەیێکی نوێ دروست دەکا |
| /pages/{page key} | `PUT` | دەستکاری پەڕە دەکا|
| /pages/{page key} | `DELETE` | پەڕەیێک دەسڕێتەوە |
| /settings | `GET` | رێکخستنەکان بلوودیت دەگەڕێنێتەوە |
| /settings | `PUT` | دەستکاری رێکخستنەکان بلوودیت دەکا |
| /images | `POST` | وێنەیێک بار دەکا و مەکینەی وێنۆچکە بۆ پەڕەیێک چالاک دەکا |
| /tags | `GET` | پێرستێک لە تاگەکان و پيريی پەیوەندی بە تاگ دەگەڕێنێتەوە |
| /tags/{tag key} | `GET` | تاگێک بە تاگێکی پەڕە دەگەرێنێتەوە |
| /categories | `GET` | هاوپۆلێک و پەڕەی هاوپۆڵ کە پەیوەندی بە کلیلی هاوپۆلێک هەیە دەگەڕێنێتەوە |
| /categories/{category key} | `GET` | هاوپۆڵ و کلیلی هاوپۆلێک دەگەڕێنێتەوە |
| /users | `GET` | پێرستی بەکارهێنەرانی تۆمارکراوە لە سیستەم دەگەڕێنێتەوە |
| /users/{username} | `GET` | پرۆفایلی بەکارهێنەر دەگەڕێنێتەوە |
| /files/{page key} | `GET` | پەڕگەکانی پەویوەند لەگەڵ پەڕە دەگەڕێنێتەوە |

<h2 id="http-response">HTTP وڵامەکان</h2>

شێوازی وڵامی بەم جۆرەیە `Content-Type: application/json`.

نرخی پێشگریمان بۆ پەڕي

| key | type | description |
|-----|------|-------------|
| status | string | Returns 0 on success. |
| message | string | Returns a little message about the execution. |
| data | array | The content of the response for the endpoint. |

<h2 id="http-status-code">HTTPدۆخی کۆدەکانی</h2>

| HTTP code | description |
|-----------|-------------|
| 200 | وڵام سەرکەوتووبوو. |
| 400 | داوا هەڵەیە،ناردراوە بی باوڕە. |
| 401 | تۆکنی API یا  ناساندنی تۆکن بزر یان هەڵەیە. |
</div>
