# wails-cross
Dockerfiles for Cross Compiling Wails Applications

Example build for linux/arm64:

    docker run --rm -v "$PWD":/usr/src/myapp -v /home/tmclane/go/src/github.com/wailsapp/wails/v2:/wails/v2 -w /usr/src/myapp wails-cross-go118:linux-arm64 /bin/sh -c 'CGO_ENABLED=1 go build -tags desktop,production'

Example build for linux/amd64:

    docker run --rm -v "$PWD":/usr/src/myapp -v /home/tmclane/go/src/github.com/wailsapp/wails/v2:/wails/v2 -w /usr/src/myapp wails-cross-go118beta2:linux-amd64 /bin/sh -c 'CGO_ENABLED=1 go build -tags desktop,production'
