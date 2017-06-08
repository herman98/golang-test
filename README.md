# golang-test
go Language Test



Please Do the following requirements before running the service
----

Setting Docker for mysql
----------
$ docker run -p 3306:3306 --name test-mysql  -e MYSQL_USER=root -e MYSQL_ROOT_PASSWORD=password -e MYSQL_DB=testDB -d mysql:latest
$ docker ps -a
$ docker start test-mysql

install and setting mysql without docker
------
$ sudo apt-get install mysql-server


install go 
-----------
$ sudo add-apt-repository ppa:gophers/go
$ sudo apt-get update
$ sudo apt-get install golang-stable

set go-path
--------
$ export GOPATH=/home/herman/App/golang/git
$ export PATH=$PATH::/usr/local/go/bin
$ export PATH=$PATH:$GOPATH/bin


go get package
-----------------
$ go get "github.com/go-sql-driver/mysql"
$ go get "github.com/gin-gonic/gin"

running service
-----
$ go run microservice.go

or using build
-----
$ go build microservice.go
$ ./microservice

