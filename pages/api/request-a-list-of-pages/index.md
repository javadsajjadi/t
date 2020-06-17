<div dir="rtl">

# داوا بۆ پێرستێک لە پەڕەکان
<!-- position: 2 -->

وەرگرتنی پێرستی پەڕەکان

تەواو داواکارییەکان بە API پێویستی بە `API Token` هەیە. Yئێوە دەتوانن تۆکن پەیدا بکەن لە API ڕێکخستنی زیادکراوەیە
</div>

```bash
Admin panel > Plugins > API > API Token
```
<div dir="rtl">
<h2 id="request">HTTP داواکان</h2>
</div>

```bash
GET /api/pages
```
<div dir="rtl">
<h2 id="parameters">پارامەتر</h2>

| key | value | Default value |
|-----|-------|---------------|
| `required` token | `string` API Token | |
| published | `boolean` پەڕەکانی بڵآوکراوە دەگەڕێنێتەوە. | `true` |
| sticky | `boolean` پەڕەکانی لکاو دەگەڕێنێتەوە. | `false` |
| static | `boolean` پەڕەکانی نەجولاو دەگەڕێنێتەوە. | `false` |
| draft | `boolean` پەڕەکانی پێش نووس دەگەڕێنێتەوە. | `false` |
| untagged | `boolean` پەڕەکان بێ تاگ دەگەرێنێتەوە. | `false` |

<h2 id="response">وڵام</h2>
</div>

```bash
HTTP Code: 200
Content-Type: application/json
Body:
{
	"status": "0",
	"message": "List of pages, amount of items: 15",
	"data": [
		{
			"key": "my-dog",
			"title": "My dog",
			"content": "...",
			"contentRaw": "...",
			"description": "...",
			"type": "published",
			"slug": "my-dog",
			"date": "2019-02-02 00:09:38",
			"dateUTC": "2019-02-02 22:09:38",
			"tags": "",
			"permalink": "https://www.example.com/my-dog",
			"coverImage": false,
			"coverImageFilename": false
		},
		{
			....
		}
	]
}
```

<div dir="rtl">
<h2 id="curl-example">CURL نمونەی فەرمانی</h2>
ئەم داوانە پەڕەکانی بڵاوکراوەو نەجوڵاو دەگەڕێنێتەوە, سنوردارە بە API. دەتوانن ژمارەی بگۆڕن لە  API ڕێکخستنەکانی.
</div>

```bash
$ curl -X GET "https://www.example.com/api/pages?token=80a09ba055b73f68e3c9e7c9ea12b432&published=true&static=true"
```

<div dir="rtl">
جەستەی داوا
</div>

```bash
{
        "status": "0",
        "message": "List of pages, number of items: 15",
        "data": [
		{
			"key": "my-dog",
			"title": "My dog",
			"content": "...",
			"contentRaw": "...",
			"description": "...",
			"type": "published",
			"slug": "my-dog",
			"date": "2019-02-02 00:09:38",
			"dateUTC": "2019-02-02 22:09:38",
			"tags": "",
			"permalink": "https://www.example.com/my-dog",
			"coverImage": false,
			"coverImageFilename": false
                },
                {
                        ....
                }
        ]
}
```

<div dir="rtl">
<h2 id="javascript-example">نمونەی جاڤا سکریپت</h2>
دەتوانن سود بگرن لە [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) بۆ وەرگرتنی پێرستی پەڕەکان.
</div>

```
<script>
	fetch("https://www.example.com/api/pages?token=eaf5df0a626145cc6d37b76f3eccc826&published=true&static=true", {
		method: 'get'
	}).then(function(response) {
		return response.json();
	}).then(function(json) {
		console.log(json.data);
	});
</script>
```
