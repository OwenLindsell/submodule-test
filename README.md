# edge-envoy-data-plane-api

This project generates Reactor GRPC bindings from Envoy [data-plane-api](https://github.com/envoyproxy/data-plane-api).

## Cloning this project
Please clone this project using the `git clone --recursive` command, to ensure the all the git submodules are also cloned.
If you forget to do this you can run `git submodule update --init --recursive` from the project root.

## How this project works
The folder `/src/main/proto` contains multiple symlinks to proto files imported as git submodules.
The root `pom.xml` generates GRPC bindings from these proto files using the `protobuf-maven-plugin`.

## Output
Running `mvn package` will create a jar containing all the GRPC bindings.
Reactor bindings are saved in files prefixed with `Reactor`
e.g. `io.envoyproxy.envoy.service.ext_proc.v3.ReactorExternalProcessorGrpc` 
