<div dir="rtl">

# وەرگرتنی تەواو تاگەکان
<!-- position: 7 -->

وەرگرتنی تاگەکان و پەڕەکان کە پەیوەندییان بە تاگەوە هەیە

تەواو داواکارییەکانی APIنیازی بە `API Token` هەیە; ئێوە دەتوانن تۆکن لە پەڕەی ڕێکخراوەکانی زیادکراوە پەیدا بکەن

<h2 id="request">وڵام</h2>

- خاڵی کۆتایی: `/api/tags`
- مێتۆد: `GET`

پێرستێک لە خاڵە کۆتاییەکان لە خوارەوە نیشان دراوە.

| key | value | Default value |
|-----|-------|---------------|
| `required` token | `string` API Token | |

<h2 id="response">وڵام</h2>

- HTTP کۆدی: `200`
- جۆری ناوەڕۆک: `application/json`
</div>

```
{
  "status": "0",
  "message": "List of tags.",
  "data": [
    {
      "name": "Bludit",
      "description": "",
      "template": "",
      "list": [
        "follow-bludit"
      ],
      "key": "bludit"
    },
    {
      "name": "CMS",
      "description": "",
      "template": "",
      "list": [
        "follow-bludit"
      ],
      "key": "cms"
    },
    {
      "name": "Flat files",
      "description": "",
      "template": "",
      "list": [
        "follow-bludit"
      ],
      "key": "flat-files"
    }
  ]
}
```

<div dir="rtl">
<h2 id="curl-example">CURLنمونە فەرمانی</h2>
گەڕانەوەی داواکان لە بڵاوکراوەکان و پەڕە نەجووڵاوەکان, سنووردارە بە API. دەتوانن ژمارەی سنوورداربوون بگۆڕن بە API رێکخستنەکانی.
</div>

```
$ curl -X GET \
	-G "https://www.example.com/api/tags" \
	-d "token=80a09ba055b73f68e3c9e7c9ea12b432"
```

<div dir="rtl">
دەرەنجام:
	</div>
```
{
  "status": "0",
  "message": "List of tags.",
  "data": [
    {
      "name": "Bludit",
      "description": "",
      "template": "",
      "list": [
        "follow-bludit"
      ],
      "key": "bludit"
    },
    {
      "name": "CMS",
      "description": "",
      "template": "",
      "list": [
        "follow-bludit"
      ],
      "key": "cms"
    },
    {
      "name": "Flat files",
      "description": "",
      "template": "",
      "list": [
        "follow-bludit"
      ],
      "key": "flat-files"
    }
  ]
}
```
	
<div dir="rtl">
<h2 id="javascript-example">نمونەی جاڤاسکریپت</h2>
دەتوانن سود بگرن لە [Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API) بۆ وەرگرتنی پێرستی تاگەکان.
</div>
	
```
<script>
	fetch("https://www.example.com/api/tags?token=eaf5df0a626145cc6d37b76f3eccc826", {
		method: 'get'
	}).then(function(response) {
		return response.json();
	}).then(function(json) {
		console.log(json.data);
	});
</script>
```
