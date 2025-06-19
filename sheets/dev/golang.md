# Go language

## Create a Go path
```bash
apt install golang-go
mkdir -p $HOME/gocode/bin
export GOPATH=$HOME/gocode
export PATH=$PATH:$GOPATH/bin

# or with Mise :
mise install golang
mise use -g go@latest

go version
```

## Get a lib
```bash
go get -v <my_lib>
```

## Useful links
* [A Tour of Go](https://tour.golang.org/welcome/1)
* [Go cheatsheet](https://devhints.io/go)
* [Fiche de secours - Golang (FR)](https://louhde.tech/cheatsheet/golang/fds-golang)
