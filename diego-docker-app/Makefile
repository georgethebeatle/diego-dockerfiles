TAG?=latest

all: dockerapp
	docker build -t cloudfoundry/diego-docker-app:${TAG} .
	rm dockerapp

dockerapp: dockerapp.go
	GOARCH=amd64 GOOS=linux go build -o dockerapp dockerapp.go
