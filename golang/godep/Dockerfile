FROM golang:1.5

MAINTAINER ckeyer <docker@ckeyer.com>

ENV APP_NAME=app
RUN mkdir /src && go get github.com/tools/godep

CMD godep go build -o /out/$APP_NAME