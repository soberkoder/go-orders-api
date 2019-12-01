*** REST API in Go

Simple CRUD service for managing orders, written in Go.


*** Setup and usage
```
cd to the project directory
```

```go
go build go-orders-api
./go-orders-api
```


Create Order
```shell
curl -H 'Content-Type: application/json' -d '{"orderedAt":"2019-11-09T21:21:46+00:00","customerName":"Tom Jerry","items":[{"itemId":"123","description":"IPhone 10X","quantity":1}]}' -X POST http://localhost:8080/orders
```

Get Orders
```shell
curl http://localhost:8080/orders
```

Update Order
```shell
curl -H 'Content-Type: application/json' -d '{"orderId":"1","orderedAt":"2019-11-09T21:21:46+00:00","items":[{"itemId":"123","description":"IPhone 10X","quantity":3}]}' -X PUT http://localhost:8080/orders/1
```

Delete Order
```shell
curl -X DELETE http://localhost:8080/orders/1
```

*** Tutorial

You can find the tutorial for this application at the [SoberKoder](https://www.soberkoder.com/) blog.

https://www.soberkoder.com/golang/golang-rest-api/
