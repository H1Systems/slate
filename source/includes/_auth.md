# Authentication

> To authorize, use this code:

```php
$url = "http://.../api/token"
$ch = curl_init();
curl_setopt(ch, "CURL_URL", $url)
```

```javascript
$.ajax(
  "url": https://faceboxx.boxxcomms.co.uk:8080/api/token
  "xhrRequest":
    {
      "withCredentials": true
    },
  "dataType": "json",
  "data": {
    "ID": username,
    "password": password
  }
)
.done(function() {

})
.fail(function() {

});
```
> Output

```
{
  "iat": *timestamp of issue*,
  "exp": *timestamp of expiration*,
  "jti": *unique string*,
  "sub": *ID of authenticated user*
}
```

> Username and Password for the token generator will be suppied when access is approved.

CORE uses JSON Web Tokens for authorisation.  You need to generate a new token before full access is granted.  You can accomplish this by using `https://faceboxx.boxxcomms.co.uk:8080/api/token`.

You need to pass basic authentication credentials (provided outside the scope of this document) and if sucessful you will be issued a JWT with a payload as defined below and in the output right...

JWT Claim|Claim Value
-|-
IAT|*timestamp of issue*
EXP|*timestamp of expairation*
JTI|*unique string used for identifying the token*
SUB|*ID of authenticated user*

## Storing the Token

```php
$ch = curl_init;
```

```javascript
$.cookie();
```

it is recomended you store the token with the following options

<aside class="notice">
To use the jQuery option in the code sample you will need the jQuery Cookies plugin https://plugins.jquery.com/cookie/
</aside>