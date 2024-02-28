### Run to generate GRPC code

    $ protoc --go_out=. --go-grpc_out=. proto/course_category.proto
    $ go mod tidy

### Install Evans to work with gRPC client

    https://github.com/ktr0731/evans
    go install github.com/ktr0731/evans@latest

### run evans client

    evans -r repl

    inside evans shell :

        show package
        package pb
        show service
        service xpto
        show message

### Call Service

        pb.CategoryService@127.0.0.1:50051> call CreateCategory

        name (TYPE_STRING) => tv
        description (TYPE_STRING) => electronics
        {
        "description": "electronics",
        "id": "86b3928d-bd5a-4fe9-ac53-83311e9007c8",
        "name": "tv"
        }
