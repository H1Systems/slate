# Campaign Engine

You can pre-save filters for use with the prospecting tools.

## Get Saved Campaign data

```php
$url = "https://faceboxx.boxxcomms.co.uk:8080/api/cEngine/fitlters";
$ch = curl_init($url);


```

```javascript
$.ajax(
	"url"		:	"https://faceboxx.boxxcomms.co.uk:8080/api/cEngine/filters",
	"dataSrc"	:	"",
	"dataType"	:	"json",
	"type"		:	"get",
	"xhrFields"	:	{ "withCredentials:true"}
);
```


To retrive existing filters use the following route with the GET method..

`https://faceboxx.boxxcomms.co.uk:8080/api/cEngine/filters[/{id}]`

The route accepts 1 argument and 1 query

Type|Name|Values
-|-|-
Argument|id|[0-9]+
Query|status|live, deleted

Without using the arguments or query all records will be retrived from the database

With the *id* argument you can select a single filter by ID

The *status* query will return either live or deleted filter records