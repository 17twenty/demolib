# demorepo

This is the companion repo to the demorepo to show how to use packages.

## Purpose ##

Barebones setup to show how a binary can be ```go getted``` and build and installed automatically.

## Usage ##
```
go get github.com/17twenty/demolib/...
```

As long as your $GOPATH/bin/ is in your $PATH you should be able to execute the binary as:

```
$ # This will allow you to test and build the binary
$ go install ./...
$ demotest 
2016/09/09 09:17:01 Here I am
```

That's it.

## Further Information ##

If you're building a library, nest your main app and put consumers of it in subdirs like this:
```
/home/nglynn/go/src/github.com/17twenty/demolib
├── cmd
│   └── demotest
│       └── main.go
├── demolib.go
└── README.md

```

Then your user can use ```go get``` to install the library, and ```go get github.com/17twenty/demolib/...``` to fetch, build and install the binaries as well.

See [this article](https://medium.com/@benbjohnson/structuring-applications-in-go-3b04be4ff091#.zag9ikesn) for more.

