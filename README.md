[![Build Status](https://travis-ci.org/wmgaca/goliath.svg?branch=master)](https://travis-ci.org/wmgaca/goliath)

# Goliath
Image processing POC written in GO:
* loads a set of images and keeps them in memory,
* provides an HTTP endpoint to check if given (posted) image exists in the set

## Prerequisites
* [Go](http://golang.org) would be nice.

## Install
```bash
mkdir [my-awsome-dir]
cd [my-awsome-dir]
export GOPATH=`pwd`
go get github.com/wmgaca/goliath
```

## Run
Run the server
```bash
bin/goliath [image-set-dir]
```

And enjoy your worthless service:
```bash
curl -i -F -filedata=~/foo/bar.png  http://localhost:8000/compare/
```

## Test

```bash
go test github.com/wmgaca/goliath/tests
```