# edge-envoy-data-plane-api

This project generates Reactor GRPC bindings from Envoy [data-plane-api](https://github.com/envoyproxy/data-plane-api).

The folder `/src/main/proto` contains multiple symlinks to proto files imported as git submodules.
The root `pom.xml` generates GRPC bindings from these proto files using the `protobuf-maven-plugin`.

Reactor bindings are saved in files prefixed with `Reactor`
e.g. `io.envoyproxy.envoy.service.ext_proc.v3.ReactorExternalProcessorGrpc` 
