# dive
- Dive in specific projects by redoing its build, test & run parts
- Learn the project in the process
- The list of projects is limited

Note: Only the projects that give a better `DevEx` to `build`, `test` & `run` any software projects of the world

### what & how
- Create project specific folders
- For example, `dive_xxx` where xxx is the actual project
- dive_xxx is configured with `.gitmodules` pointing to xxx
  - refer: https://github.com/runfinch/finch-core
  - refer: https://github.com/runfinch/finch
- Similarly, `dive_containers` can replicate `testcontainers` model of testing the published containers
  - refer: https://github.com/testcontainers/testcontainers-go/tree/main/modules
- On the whole, verify these projects with your own innovative techniques
- Your techniques may vary
- For example, you may use either or all of the below approaches to dive into a project:
  - use of golang code,
  - use of testcontainers,
  - use of bakefile (from makers of docker),
  - use of unikernels,
  - & so on.

Note that verifying is an exercise to dive deep into the internals of the project

### prioritised / dive in these projects
- https://github.com/abiosoft/colima
- https://github.com/lima-vm/lima
- https://github.com/testcontainers/testcontainers-go/tree/main/modules
- 
- # reflect back before trying further #
- 
- https://github.com/containerd/containerd
- runc
- https://github.com/runfinch/finch-core
- https://github.com/runfinch/finch
- 
- # reflect back before trying further #
- 
- https://github.com/abiosoft/colima
- https://github.com/dagger/dagger/tree/main/examples/sdk/go
- buildkit
- unikraft / kraftkit?

### project list
_Note: Keep categorising & prioritising & pruning this list_

- https://github.com/testcontainers/testcontainers-go
- refer: https://go.googlesource.com/vuln/+/refs/tags/v1.0.1/all_test.go
- 
- https://github.com/unikraft/kraftkit/tree/staging
- https://github.com/opencontainers/runc/tree/main
- https://github.com/containerd/nerdctl/releases
- https://github.com/vmware/vic
- https://github.com/siderolabs/talos
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

### Similarity
I think it will be `finch` & `lima` the hard way
