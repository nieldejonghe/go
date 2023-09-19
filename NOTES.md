# Go Notes

* go and git are tightly coupled ...
* using gh cli to create repo: ` gh repo create ` 
* use Apache License 2.0. 
* go was developed for the biggest tech enteprises in history
* go is the standard for cloud native computing.
* most cloud native tools are written in go (Kubernetes, helm, ...) 
* helm templating is created with go templating, same with hugo for static html creation.
* check (github.com/rwxrob/awesome-go)

## How to install Go 

Install however but make sure it is 1.21+, most package managers are way behind on the version. 

* `brew install golang-go`
* `apt install go`
* or get the latest version from the go website

## How to start a Go project

* go mod init github.com/nieldejonghe/ga
* go mod tidy 

* am I writing a package? or am I writing a command?
you either are writing a command, this is when you have a main function or you have a module/package.
In this case we will start with a command. 

* touch main.go (when it's a package use the name of the package, or lib.go) 
* now it's time to start coding!!

## Go rules

* Every single file that ends in .go must have a package name. This is mandatory by the compiler. 
* `package main` is only used by things that turn into executable commands.
* In go you can't use single quotes, these are only for runes, a rune is a data type that stores code that represent unicode characters.
* make sure to import packages when you are using them, go will not compile when there is stuff that is unused (variables, packages,...)
* you can run go without compiling when using `go run main.go` 
* `go build` this will create a binary that matches the name of the parent directory.
* you can also use `go build -o <name>` 
* now you can run the program with ` ./go ` in our case
* hyperfine is a good benchmark tool, for example to compare go vs shell script.
* `go env` shows you all the go environment vars
* `go install` will install it in your gobin directory.
* most of the time you should be making a package which a command uses.
* you can EXPORT a package by using an uppercase. (Every single function should be exported? how to hide them?)
