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

`/enter/`
* Method: `POST`
* Data params: `code=12345`
* Success response:
  * Code: 200

```javascript
{"status":true}
```
* Error responses:
  * Code: 400
```javascript
{"status":false,"code":"lc1","message":"Wrong login code"}
```
```javascript
{"status":false,"code":"lc2","message":"No login code"}
```

`/code/`
* Method: `POST`
* Data params: `pattern[]=0&pattern[]=1&pattern[]=2&digits[]=1&digits[]=2&digits[]=3`
* Pattern code: 123456789
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
`/data/summary`
* Method: `GET`
* Success response:
  * Code: 200

```javascript
{"status":true,"content":{"balance":78036,"funds":91923,"payments":87511}}
```

`/data/history`
* Method: `GET`
* Success response:
  * Code: 200

```javascript
{"status":true,"content":[{"id":"B48YL","date":"1923-07-24T04:33:07.596Z","description":"etiam aliquam aliquam","category":"Cash","currency":"PLN","amount":238,"status":"income"}]}
```

`/data/products`
* Method: `GET`
* Success response:
  * Code: 200

```javascript
{"status":true,"content":[{ "type": "Wallet", "currency": "PLN", "amount": 489.50 }]}
```

`/data/budget`
* Method: `GET`
* Success response:
  * Code: 200

```javascript
{"status":true,"content":{"year":2016,"months":[{"month":0,"summary":{"sum":314,"total":3275},"other":4764,"elements":[{"food":{"amount":677,"limit":3706,"value":481},"home":{"amount":677,"limit":3706,"value":481},"car":{"amount":677,"limit":3706,"value":481}}]}]}}
```

`/data/chart`
* Method: `GET`
* Success response:
  * Code: 200

```javascript
{"status":true,"content":[{"date":"2005-10-04T16:42:59.395Z","description":"ipsum tortor vestibulum","currency":"EUR","amount":773,"status":"income"}]}
```

