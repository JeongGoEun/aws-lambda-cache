# Memory caching server

[![GoDoc](https://godoc.org/github.com/hexoul/aws-lambda-cache?status.svg)](https://godoc.org/github.com/hexoul/aws-lambda-cache)

Simple memory cache server on AWS lambda

## Contents
- [Usage](#usage)
- [Build](#build)
- [Test](#test)
- [Deploy](#deploy)
- [License](#license)

## Usage
1. Set value
  - GET: url?key=[key]&val=[val]
  - POST: url?key=[key]
2. Get value
  - GET: url?key=[key]

## Build
```shell
dep ensure
make
```

## Test
```shell
go test -v
```

## Deploy
1. Set Lambda on AWS
  - Function package: compressed binary file in $GOPATH/src/{repo}/bin
  - Handler: cache (binary file name, it is optional)
  - Runtime: Go 1.x
2. Set API Gateway for cache server on AWS
3. Add API Gateway as Lambda trigger
4. Add CloudWatch Logs

## License
MIT
