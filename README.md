## Rootless Container from scratch

> written in Go

### Steps to run

> must be run as a non root user.

Configured to run with UID 1000 and GID 1000. You'll have to change if you want a different uid and gid

#### Step 1

Create a alpine based fs at `/home/abhaybhargav/alpine-fs` for the filesystem mount. Please replace `abhaybhargav` for your user's home directory or any other directory

#### Step 2

```bash

go run main.go run /bin/bash

```

> puts you into a shell on the "container" with its own namespace, PID and UTS separation, in a separate user namespace. 

> you'll not have CGroup capability
