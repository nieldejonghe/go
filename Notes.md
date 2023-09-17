# Go Notes

* go and git are tightly coupled ...
* using gh cli to create repo: ` gh repo create ` 
* use Apache License 2.0. 
* go was developed for the biggest tech enteprises in history
* go is the standard for cloud native computing.
* most cloud native tools are written in go (Kubernetes, helm, ...) 
* helm templating is created with go templating, same with hugo for static html creation.
* check (github.com/rwxrob/awesome-go)

## How to install go 

Install however but make sure it is 1.21+, most package managers are way behind on the version. 

* `brew install golang-go`
* `apt install go`
* or get the latest version from the go website

## How to start a go project

* go mod init github.com/nieldejonghe/ga
* go mod tidy 

* am I writing a package? or am I writing a command?
you either are writing a command, this is when you have a main function or you have a module/package.
In this case we will start with a command. 

* touch main.go (when it's a package use the name of the package, or lib.go) 
* now it's time to start coding!! 
 
