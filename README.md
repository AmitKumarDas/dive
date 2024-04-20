# dive
Dive into a project & learn in the process

### What
- Create project specific folders
- Start with projects that are used across e.g. finch, buildkit, containerd, runc, etc
- Verify these projects based on your techniques
- Verifying is an exercise to dive deep into the internals of the project

### How
- Verify public APIs/SDKs using Golang's example_test.go
- Verify public APIs/SDKs using Golang's testing.T & other standard packages
- Verify running the projects via lima, containers, unikernels, etc.

### Now
- Start with https://github.com/runfinch/finch
- Finch might help you learn nerdctl + Buildkit + containerd + runc
- Try experimenting / redoing finch via functional options pattern
- Apply unit testing, testcontainers whereever possible

### Later
- unikraft / kraftkit?
- Dagger e.g. https://github.com/dagger/dagger/tree/main/examples/sdk/go

### Interesting Project List
_Note: Keep categorising & prioritising & pruning this list_

- https://github.com/testcontainers/testcontainers-go
- refer: https://go.googlesource.com/vuln/+/refs/tags/v1.0.1/all_test.go
- 
- https://github.com/unikraft/kraftkit/tree/staging
- https://github.com/opencontainers/runc/tree/main
- https://github.com/containerd/nerdctl/releases
- https://github.com/vmware/vic
- 
- https://pkg.go.dev/golang.org/x/mod@v0.14.0/modfile
- https://go.googlesource.com/vuln/+/refs/tags/v1.0.1/scan/scan.go
- https://github.com/siderolabs/kres/tree/main
- https://github.com/bracesdev/errtrace
- https://github.com/canonical/chisel/tree/main
- 
- https://github.com/GoogleContainerTools/container-structure-test/tree/main/pkg/drivers
- https://github.com/testcontainers
- https://github.com/dagger/dagger/tree/main/examples/sdk/go
- https://github.com/runfinch/finch

### Summary
Given my interest areas, one may find me `building`, `testing` & `running` a project X using project X
