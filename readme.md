
# URL Shortener - Python

A URL Shortener build in Python with FastAPI.
<br>
<br>


Example of response after a request with a long URL:

```JSON
{
  "target_url": "https://github.com",
  "is_active": true,
  "clicks": 0,
  "url": "http://127.0.0.1:8000/ZYKL6",
  "admin_url": "http://127.0.0.1:8000/admin/ZYKL6_58HE7BEH"
}
```
<BR>

## API Reference
___

#### Root

```http
  GET /
```
<br>
___
<br>

#### Create an URL

```http
  POST /url
```

| Parameter    | Type     | Description                                 |
| :----------- | :------- | :------------------------------------------ |
| `target_url` | `string` | The response will contain the shortened URL |

___
<br>

#### Forward to target URL

```http
  GET /{url_key}
```

| Parameter | Type     | Description |
| :-------- | :------- | :---------- |
| `url_key` | `string` | -           |


___
<br>

#### Get administration info

```http
  GET /admin/{secret_key}
```

| Parameter    | Type     | Description                                                              |
| :----------- | :------- | :----------------------------------------------------------------------- |
| `secret_key` | `string` | Will return info about shortened URL (nº of clicks, target URL and more) |

___
<br>

#### Delete URL

```http
  DELETE /admin/{secret_key}
```

| Parameter    | Type     | Description                   |
| :----------- | :------- | :---------------------------- |
| `secret_key` | `string` | Will delete the shortened URL |

___
<br>

## Next optimizations

* Containerize the application
* Code refactoring
