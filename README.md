# goamz - An Amazon Library for Go

[![Build Status](http://travis-ci.org/goamz/goamz.png?branch=master)](https://travis-ci.org/goamz/goamz)

The _goamz_ package enables Go programs to interact with Amazon Web Services.

This is a fork of the version [developed within Canonical](https://wiki.ubuntu.com/goamz) with additional functionality and services from [a number of contributors](https://github.com/golangbox/goamz/contributors)!

The API of AWS is very comprehensive, though, and goamz doesn't even scratch the surface of it. That said, it's fairly well tested, and is the foundation in which further calls can easily be integrated. We'll continue extending the API as necessary - Pull Requests are _very_ welcome!

The following packages are available at the moment:

```
github.com/golangbox/goamz/autoscaling
github.com/golangbox/goamz/aws
github.com/golangbox/goamz/cloudformation
github.com/golangbox/goamz/cloudfront
github.com/golangbox/goamz/cloudwatch
github.com/golangbox/goamz/dynamodb
github.com/golangbox/goamz/ecs
github.com/golangbox/goamz/ec2
github.com/golangbox/goamz/elb
github.com/golangbox/goamz/iam
github.com/golangbox/goamz/rds
github.com/golangbox/goamz/route53
github.com/golangbox/goamz/s3
github.com/golangbox/goamz/sqs
github.com/golangbox/goamz/sts

github.com/golangbox/goamz/exp/mturk
github.com/golangbox/goamz/exp/sdb
github.com/golangbox/goamz/exp/sns
```

Packages under `exp/` are still in an experimental or unfinished/unpolished state.

## API documentation

The API documentation is currently available at:

[http://godoc.org/github.com/golangbox/goamz](http://godoc.org/github.com/golangbox/goamz)

## How to build and install goamz

Just use `go get` with any of the available packages. For example:

* `$ go get github.com/golangbox/goamz/ec2`
* `$ go get github.com/golangbox/goamz/s3`

## Running tests

To run tests, first install gocheck with:

`$ go get gopkg.in/check.v1`

Then run go test as usual:

`$ go test github.com/golangbox/goamz/...`

_Note:_ running all tests with the command `go test ./...` will currently fail as tests do not tear down their HTTP listeners.

If you want to run integration tests (costs money), set up the EC2 environment variables as usual, and run:

$ gotest -i
