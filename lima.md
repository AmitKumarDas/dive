## lima learnings

### downloads & digests - practices / 21-APR-2024
```yaml
- design: entities: arch, digest, location
- design: log: Attempting to download
- design: path: see below logs on how `location` is defined
```
```sh
INFO[0000] Attempting to download the nerdctl archive
arch=aarch64
digest="sha256:ff38142440b4705e12782b7a71074849e712a42ccb69a11306343a8d9f81d8ab"
location="https://github.com/containerd/nerdctl/releases/download/v1.7.5/nerdctl-full-1.7.5-linux-arm64.tar.gz"
```

### access vm disk by mounting the qcow2 & extract files off it
```yaml
images:
  - location: "https://cloud.debian.org/images/cloud/sid/daily/latest/debian-sid-genericcloud-arm64-daily.qcow2"
    arch: "aarch64"
mounts:
  - location: "~"
  - location: "/tmp/lima"
    writable: true
mountType: virtiofs
vmType: vz
```

### hostagent socket location
```sh
$ /Users/cjs/.lima/default/ha.sock
```
### troubleshooting/ generic
```yaml
- limactl start --video # might show errors
```
