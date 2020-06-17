<div dir="rtl">
	
# دروستکردنی پەڕەیێکی نوێ
<!-- position: 4 -->

دروستکردنی پەڕەی نوێ.

تەواو داواکارییەکان بۆ  API نیازمەندی `API Token` ـە. ئێوە دەتوانن تۆکن لە  ڕێکخراوەی زیادکراوەی ئەی.پی.ئەی پەیدا بکەن
</div>

```bash
Admin panel > Plugins > API > API Token
```

<div dir="rtl">
تەواو داواکان بۆ نووسینین API بۆ ناوەرۆک, ئێوە دەبێ  `Authentication Token` فەراهەم بکەن.بۆ بەدەستکەوتنی تۆکن ئێوە پێویستان بە بەکارهێنەرێک بە ڕۆڵێ `Administrator` هەیە.دەتوانن `Authentication Token` لە پرۆفایلی بەکارهێنەر وەربگرن
</div>

```bash
Admin panel > Manage > Users > {Username} > Security > Authentication Token
```

<div dir="rtl">
<h2 id="request">HTTPداواکان</h2>
</div>

```bash
POST /api/pages/{key}
```

<div dir="rtl">
<h2 id="parameters">پارامەتر</h2>

| key | value | Default value |
|-----|-------|---------------|
| `required` token | `string` API Token. | |
| `required` authentication | `string` Authentication token. | |
| title | `string` سەردێڕی پەڕە. | |
| content | `string` ناوەڕۆکی پەڕە. | |
| tags | `string` تاگەکانی پەڕە جودای بکە بە بۆر . | |
| type | `string` جۆری پەڕە. | |
| date | `string` رێکەوتی پەڕە (شێواز بە م جۆرەیە "YYYY-MM-DD Hours:Minutes:Seconds"). | |
| slug | `string` ناونیشانی ناوی لاتینی پەڕە. | (Derived from lowercased title) |
| dateModified | `string` بەرواوری دەستکاری پەڕە. | |
| position | `string` شوێنی پەڕە. | |
| coverImage | `string` وێنەی بەرگی پەڕە. | |
| category | `string` هاوپۆلی پەڕە. | |
| template | `string` رووکاری پەڕە. | |
| noindex | `string` پەڕەی پشت. | |
| nofollow | `string` پەڕەی شوێن نەکەوتوو. | |
| noarchive | `string` پەڕەی ئارشیڤ نەکراو. | |

<h2 id="response">وڵام</h2>
</div>

```bash
HTTP Code: 200
Content-Type: application/json
Body:
{
	"status": "0",
	"message": "Page created.",
	"data": {
		"key": "<page key>"
	}
}
```

<div dir="rtl">
<h2 id="curl-example">CURLنمونە فەرمانی </h2>
لێرە پێتان نیشان دەدرێ دروستکردنی پەڕەیێکی نوێ بە فەرمان لە سەر `curl` . پەڕگەی `data.json` زانیاری بنەڕەتی تێدایە بۆ دروستکردنی پەڕەی نوێ.

ناوەڕپکی پەڕەی `data.json`:
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
جیبەجێی بکەن فەرمانەکان لە پەڕگەی `data.json` :
</div>

```bash
$ curl  -X POST \
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
	"message": "Page created.",
	"data": {
		"key": "my-dog"
	}
}
```
