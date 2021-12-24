# Test case for https://github.com/swaggest/rest/pull/50 #

```
go run .

curl --request PUT --url http://localhost:8011/hello/iain --header 'content-type: application/json' --data '{"expiryDate": null}'
```

Output:
```
{"status":"INVALID_ARGUMENT","error":"invalid argument: validation failed","context":{"body":["#/expiryDate: %!q(<nil>) is not valid \"date-time\""]}}
```
