# voting

In this application we will save the request in the Postgres database, but for do it, first we send the request to a RabbitMQ exchange and a consumer will process it and save in the database.

## Dependencies
we can use the docker image to RabbitMQ and Posgresql.


## How to start
In the root of the application run the command of the program that will send the message to the RabbitMQ:

`go run main.go`

After that, enter in the consumer directory and run:

`go run main.go`

Example of the request to the api:

```
curl -d '{"name":"Phoenix"}' -H "Content-Type: application/json" -X POST http://localhost:8080/api/votes
``````