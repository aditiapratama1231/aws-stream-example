# AWS Kinesis Data Stream With GoLang
This repositories was created to provide the way to send and get data to and from aws kinesis with go programming langange (golang). We will using `kinesis-local` docker image to get simulation of aws kinesis in local computer. 

This project was devided to be three sub folder : 
- `consumer` to consume data from kinesis
- `producer` to product data to kinesis
- `stream` to create or delete streaming name

## How to run ?
Note : If you have already installed `Kinesalite` on local, please use that instead of using docker

Build:
- `docker build -t kinesis-local .` or you can use docker image in https://hub.docker.com/r/ruanbekker/kinesis-local

Run and expose port 4567:
- `docker run -it -p 4567:4567 kinesis-local:latest`

Create or delete stream name :
- Move to `stream` folder to create or delete stream name
- `go build stream.go ` to create new stream.
- create : `./stream -action=create`
- delete : `./stream -action=delete`

After Create Stream 

Send data stream :
- Move to producer folder to produce/send data to kinesis and `go run produce.go`. In this folder, you will see `Data` folder, it contains data structure, just copy that to `data.json`.

GOOD LUCK :)