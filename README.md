# playground

[![Build Status](https://travis-ci.org/gofunky/playground.svg?branch=master)](https://travis-ci.org/gofunky/playground)
[![Go Report Card](https://goreportcard.com/badge/github.com/gofunky/playground)](https://goreportcard.com/report/github.com/gofunky/playground)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/968f720de11348cf966e192fa9c9da76)](https://www.codacy.com/app/gofunky/playground?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=gofunky/playground&amp;utm_campaign=Badge_Grade)

This subrepository holds the source for the Go playground:
https://play.golang.org/

## Building

```
# build the image
docker build -t playground .
```

## Running

```
docker run --name=play --rm -d -p 8080:8080 playground
# run some Go code
cat /path/to/code.go | go run client.go | curl -s --upload-file - localhost:8080/compile
```

# Deployment

```
gcloud --project=golang-org --account=person@example.com app deploy app.yaml
```

# Contributing

To submit changes to this repository, see
https://golang.org/doc/contribute.html.
