### **GOROOT**: `/usr/lib/go`
> It is the location of your GO SDK. GO binary distribution assumes this location to be /usr/local/go for Linux/MAC platforms and  c:\Go for Windows. But GO SDK can also be installed in a custom location. In case it is installed to a custom location, then GOROOT should point to that directory.  GOROOT should only be set when installing GO to a custom location or when you want to maintain different versions of GO

### **GOPATH**: `/home/super/go/`
> The discussion for GOPATH will revolve around whether you are using GO version 1.13 higher or lower. In version 1.13, GO introduced a new feature for dependency management called GO modules. Let’s first understand the legacy behavior of GOPATH and then we will discuss what has changed with respect to GOPATH after GO version 1.13.

**Before Go Version 1.13**
> The GOPATH env variable was used for resolving go imports statements as well as it also specifies the location of your GO workspace. It is the root of GO workspace. A dependency cannot be imported if it is not inside GOPATH. Hence earlier version required all your source code to be inside GOPATH. So basically GOPATH is used for

**After Go Version 1.13**
> In version 1.13, GO announced a new feature of dependency management called GO modules. We will learn about this feature in upcoming tutorials. For now, you can imagine that with the new feature, GO doesn’t require putting all GO code in the Go workspace or in the $GOAPTH/src directory. You can create the directory anywhere and put your Go program there. Note that all legacy behavior of GOPATH is still valid for version 1.1.3 and higher.  Also note that with this new GO module feature, GO programs can be run in two ways.

Refer to the [page](https://golangbyexample.com/workspace-hello-world-golang/) for more information on sub directories and such.

### **$GOBIN**: `/home/super/go/bin/`
> GOBIN env variable specifies the directory where go will place the compiled application binary after building the main package. It defaults to $GOPATH/bin or $HOME/go/bin if the GOPATH environment variable is not set.  Also it is good idea to add GOBIN path to PATH env as well so that binary installed can be run without specifying full path of the binary. Set GOBIN in the ~/.$HOME/.profile file and add it to PATH as well.

### The three ways to run a go file.
1. `go install` - Create a binary in $GOBIN.
2. `go build` - Create a binary in the current directory.
3. `go run file.go` - Compile and run the go file in the current directory.

To run compiled files, simply type their name. In the example of, `file.go`, it would be `file`.
