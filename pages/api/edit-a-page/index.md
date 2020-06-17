<div dir="rtl">

# دەستکاری پەڕەیێک
<!-- position: 5 -->

دەتکاری پەرەیێک
Aتەواو داواکان لە سەر API پێویستیان بە `API Token`. ئێوە دەتوانن تۆکن پەیدا بکەن لە API ڕێکخستنی زیادکراوەی
</div>

```bash
Admin panel > Plugins > API > API Token
```

<div dir="rtl">
بۆ تەواو داواکارییەکانی API بۆ نووسینی ناوەرۆک, پێویستان بە نیشاندانی `Authentication Token` هەیە. بۆ وەرگرتنی ئەم تۆکنە, پێویستان بە بەکارهێنەرێک بە ئاستی `Administrator` هەیە. وەریبگرن `Authentication Token` لە پرۆفایلی بەکارهێنەر
</div>

```bash
Admin panel > Manage > Users > {Username} > Security > Authentication Token
```

<div dir="rtl">
<h2 id="request">HTTP داوای</h2>
</div>

```bash
PUT /api/pages/{key}
```

<div dir="rtl">
<h2 id="parameters">پارامەتر</h2>

| key | value | Default value |
|-----|-------|---------------|
| `required` token | `string` API Token. | |
| `required` authentication | `string` Authentication token. | |
| title | `string` سەردێڕی پەڕە. | |
| content | `string` ناوەڕۆکی پەڕە. | |
| tags | `string` تاگەکانی پەڕە. | |
| type | `string` جۆری پەڕە. | |
| date | `string` بەرواری پەڕە. | |
| dateModified | `string` بەرواری دەستکاری پەڕە. | |
| position | `string` شوێنی پەڕە. | |
| coverImage | `string` وێنە بەرگی پەڕە. | |
| category | `string` هاوپۆلی پەڕە. | |
| template | `string` رووکاری پەڕە. | |
| noindex | `string` پەڕەی پشت. | |
| nofollow | `string` پەڕەی شوێن نەکەوتوو. | |
| noarchive | `string` پەڕەی بێ ئارشێڤ. | |

<h2 id="response">وڵام</h2>
</div>

```bash
HTTP Code: 200
Content-Type: application/json
Body:
{
	"status": "0",
	"message": "Page edited.",
	"data": {
		"key": "<page key>"
	}
}
```

<div dir="rtl">
<h2 id="curl-example">CURLنمونە فەرمانی</h2>
پەیرەوەی لە نمونەی curl نیشاندەدرێت چۆن دەستکاری پەڕەیێک بە کلیلی `my-dog` بکەن.

ناوەڕۆکی پەڕگەی `data.json`
</div>

```bash
{
	"token": "24a8857ed78a8c89a91c99afd503afa7",
	"authentication": "193569a9d341624e967486efb3d36d75",
	"title": "My dog",
	"content": "Content of the page here, support Markdown code and HTML code."
}
```

<div dir="rtl">
جێبەجێکردنی فەرمان, و لکاندنی پەڕەگەی `data.json` :
</div>

```bash
$ curl  -X PUT \
	-H "Content-Type: application/json" \
	-d @data.json \
	"https://www.example.com/api/pages/my-dog"
```

<div dir="rtl">
جەستەی وڵام
</div>

```bash
{
	"status": "0",
	"message": "Page edited.",
	"data": {
		"key": "my-dog"
	}
}
```
