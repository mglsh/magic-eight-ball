# `magic-eight-ball` Repository

> The `magic-eight-ball` repository is a very simple RESTful API written in the [Go Programming Language](https://go.dev/) 
> and using the [Gin Web Framework](https://gin-gonic.com/docs/). The goal is to provide a URI which contains all 20 
> of the original [Magic 8-ball](https://en.wikipedia.org/wiki/Magic_8-ball) answers, plus a second URI will provide a 
> random answer - to mimic the functionality of the original toy manufactured by [Mattel](https://en.wikipedia.org/wiki/Mattel).

## Publications

This repository is related to the following DZone.com publications:

* [Using Render and Go for the First Time](https://dzone.com/articles/using-render-and-go-for-the-first-time)
* [Under the Hood: Render Unified Cloud](https://dzone.com/articles/under-the-hood-render-unified-cloud)

To read more of my publications, please review one of the following URLs:

* https://dzone.com/users/1224939/johnjvester.html
* https://johnjvester.gitlab.io/dZoneStatistics/WebContent/#/stats?id=1224939

## Starting the `magic-eight-ball` Repository

With the Go programming language installed, simply use the following command to start the simply RESTful API:

```shell
go run .
```

The service should start, providing information similar to what is displayed below:

```shell

                                d8b                .d8888b.         888               888 888
                                Y8P               d88P  Y88b        888               888 888
                                                  Y88b. d88P        888               888 888
88888b.d88b.   8888b.   .d88b.  888  .d8888b       "Y88888"         88888b.   8888b.  888 888
888 "888 "88b     "88b d88P"88b 888 d88P"         .d8P""Y8b.        888 "88b     "88b 888 888
888  888  888 .d888888 888  888 888 888           888    888 888888 888  888 .d888888 888 888
888  888  888 888  888 Y88b 888 888 Y88b.         Y88b  d88P        888 d88P 888  888 888 888
888  888  888 "Y888888  "Y88888 888  "Y8888P       "Y8888P"         88888P"  "Y888888 888 888
                            888
                       Y8b d88P
                        "Y88P"


GoVersion: go1.17.6
GOOS: darwin
GOARCH: amd64
NumCPU: 16
GOPATH: /Users/john.vester/go
GOROOT: /usr/local/go
Compiler: gc
ENV: /Users/john.vester/go
Now: Monday, 17 Jan 2022

[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /answers                  --> main.getAllAnswers (3 handlers)
[GIN-debug] GET    /answer                   --> main.getRandomAnswer (3 handlers)
```

## Using the `magic-eight-ball` Repository

Simply perform GET requests to the following URIs:

* /answers - provides a list of all 20 original Magic 8-ball answers
* /answer - returns a random answer from the 20 original Magic 8-ball options

For example, the following request:

```shell
curl http://localhost:8080/answer
```

Could return the following response:

```json
{
    "id": 5,
    "response": "You may rely on it."
}%
```

## Additional Information

Made with <span style="color:red;">♥</span> &nbsp;by johnjvester@gmail.com, because I enjoy writing code.
