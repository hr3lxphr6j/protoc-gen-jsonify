# protoc-gen-jsonify

Adds encoding/json Marshaler and Unmarshaler methods on PB messages that utilizes the more correct jsonpb package.
See: https://godoc.org/github.com/golang/protobuf/jsonpb

From: https://github.com/lyft/protoc-gen-star/tree/master/testdata/protoc-gen-example

## Installation

```shell
go get github.com/hr3lxphr6j/protoc-gen-jsonify
```

## Parameters

- `jsonpb`: specify the jsonpb lib which you what to use, default is `github.com/golang/protobuf/jsonpb`

## Examples

```shell
protoc \
    -I . \
    --go_out=":../generated" \
    --jsonify_out="jsonpb=github.com/gogo/protobuf/jsonpb:../generated" \
    example.proto
```
