# Efigence Camp 2016 REST API

## End-points:

`/login/`

* Method: `POST`
* Data params: `login=efi&password=camp`
* Success response:
  * Code: 200

```javascript
{"status":true}
```
* Error responses:
  * Code: 400
```javascript
{"status":false,"code":"l1","message":"No login\/password"}
```
```javascript
{"status":false,"code":"l2","message":"Wrong login\/password"}
```

`/code/`
* Method: `POST`
* Data params: `pattern[]=0&pattern[]=1&pattern[]=2&digits[]=1&digits[]=2&digits[]=3`
* Success response:
  * Code: 200

```javascript
{"status":true}
```
* Error responses:
  * Code: 400
```javascript
{"status":false,"code":"c1","message":"Wrong or no pattern\/digits"}
```
```javascript
{"status":false,"code":"c2","message":"Wrong match"}
```
