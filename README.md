# protos

Shared gRPC contract (`.proto` files) between `movie-service` and `people-service`.

This repo contains only `.proto` files. Each service includes it as a git submodule at `proto/` and generates its own Kotlin stubs at build time, so no generated code is committed here.

## Updating the contract

1. Change the `.proto` files here, then commit and push.
2. In each service, run `git submodule update --remote proto` and commit the new submodule pointer.
