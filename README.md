# yogoa [![Build Status](https://travis-ci.org/jackwakefield/yogoa.svg?branch=master)](https://travis-ci.org/jackwakefield/yogoa) [![Coverage Status](https://coveralls.io/repos/github/jackwakefield/yogoa/badge.svg?branch=master)](https://coveralls.io/github/jackwakefield/yogoa?branch=master) [![Yoga Version](https://img.shields.io/badge/Yoga-1.10.0-lightgrey.svg)](https://github.com/facebook/yoga)

A Go wrapper for Facebook's [Yoga](https://github.com/facebook/yoga) layout engine.

Bindings generated with [c-for-go](https://github.com/xlab/c-for-go).

## Todo

- Documentation

## Missing

- Logging (cgo lacks support for variadic parameters)
- Assert (unnecessary?)

## Tutorial
```

go get -u github.com/xlab/c-for-go

./scripts/download-yoga.sh

??? sed -i ".bak" "s/jackwakefield/facebook/g" `grep -lr 'jackwakefield' ./pkg/yogoa/`

docker build -t yogoa/watir ./test

c-for-go --ccincl -out ./pkg ./yoga.yml

    vi test/gentest.rb 注释# 52～56
  
docker run -i -v $(pwd):/yogoa yogoa/watir ./test/gentest.rb

goimports -w pkg/yogoa/yoga_test.go

go test -v -race ./...

```
