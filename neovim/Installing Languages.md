## Installing golang
1. Download [go1.22.5.linux-amd64.tar.gz](https://go.dev/dl/go1.22.5.linux-amd64.tar.gz)  `curl -LO https://go.dev/dl/go1.22.5.linux-amd64.tar.gz`
2. Run to install `sudo tar -C /usr/local -xzf go1.22.5.linux-amd64.tar.gz`
3. Export path `echo 'export PATH=$PATH:/usr/local/go/bin' >> ~/.zshrc` ***This directory contains the Go programming language binaries (e.g., `go`, `godoc`, `gofmt`) after you install the Go language itself from a tarball or package***
4. Add the following line at the end of the file `echo 'export PATH=$PATH:~/go/bin' >> ~/.zshrc` ***When you install Go packages using `go install`, the binaries are typically placed in this directory if the `GOPATH` environment variable is set to the default (i.e., `~/go`).***
5. Source the file `source $HOME/.profile` or `source ~/.zshrc`