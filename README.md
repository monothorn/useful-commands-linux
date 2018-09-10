# useful-commands-linux
Commands I like to use.
-----------------------------------------------------------------------------------------------------------------


1. List all available services on an ubuntu system
```
service --status-all

 [ + ]  acpid
 [ + ]  apparmor
 [ + ]  apport
 [ + ]  atd
 [ - ]  bootmisc.sh
 [ - ]  checkfs.sh
 [ - ]  checkroot-bootclean.sh
 [ - ]  checkroot.sh
 [ - ]  console-setup

```
2. List all remote branches for a repo

```
git status -r

origin/develop
origin/feature/f1
origin/feature/f2
```


3. Building docker images with static go builds

```
Step 1 : Build go image
CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o ../../build/consumer/consumer .
CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo -o ../../build/producer/producer .


Step 2 : Build docker image
sudo docker build -t k_producer -f Dockerfile .
sudo docker build -t k_consumer -f Dockerfile .

Step 3 : Run docker image

```
