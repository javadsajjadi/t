<div dir="rtl">

# داوا بۆ پەڕەییکی تایبەت
<!-- position: 3 -->

بۆ وەرگرتنی کلیلی پەڕەیێکی تایبەت

تەواوی داواکان بۆ API پێویستی بە `API Token` هەیە. ئێوە دەتوانن تۆکن لە پەڕەی رێکخستنی ئەی.پی.ئەی پەیدا بکەن
</div>

```bash
Admin panel > Plugins > API > API Token
```
<div dir="rtl">
<h2 id="request">HTTP داواکان</h2>
</div>

```bash
GET /api/pages/{page key}
```

<div dir="rtl">
<h2 id="parameters">Parameters</h2>

| key | value | Default value |
|-----|-------|---------------|
| `required` token | `string` API Token | |


<h2 id="response">وڵام</h2>
</div>

```bash
HTTP Code: 200
Content-Type: application/json
Body:
{
	"status": "0",
	"message": "Page filtered by key: my-dog",
	"data": {
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
	}
}
```

<div dir="rtl">
<h2 id="curl-example">CURL نمونە فەرمانی</h2>
ئێوە دەتوانن داوای پەڕەییکی تایبەت بکەن بە کلیلیکی تایبەت

لەم نمونەیە ئێوە دەتوانن داوای پەڕەیێک بە کلیلیل `my-dog` بکەن.
</div>

```bash
$ curl -X GET "https://www.example.com/api/pages/my-dog?token=80a09ba055b73f68e3c9e7c9ea12b432"
```
<div dir="rtl">
جەستەی وڵام
</div>

```bash
{
	"status": "0",
	"message": "Page filtered by key: my-dog",
	"data": {
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
	}
}
```

<div dir="rtl">
<h2 id="javascript-example">نمونەیە جاڤاسکریپت</h2>
دەتوانن سود لە  [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) بۆ وەرگرتنی پەڕە بگرن.
</div>

```bash
<script>
	fetch("https://www.example.com/api/pages/my-dog?token=eaf5df0a626145cc6d37b76f3eccc826", {
		method: 'get'
	}).then(function(response) {
		return response.json();
	}).then(function(json) {
		console.log(json.data);
	});
</script>
```
