# again

> "Insanity is doing the same thing over and over again and expecting different results." –*not* Albert Einstein

Run a command until it succeeds (or fails), again and again.

This is a fork from an [original project by @yansal](https://github.com/yansal/again).

## Installation

```console
go get -u github.com/falzm/again
```

## Usage

```console
$ again -h
Usage of again:
  -fail
 	run until command fails
  -silent
 	don't print failed attempts error message
  -sleep duration
 	how long to sleep before running again?
```

Example: try to connect to a rebooting server

```console
$ again ssh -o ConnectTimeout=3 myserver.example.net
again: main.go:39: exit status 255
ssh: connect to host 1.2.3.4 port 22: Operation timed out
again: main.go:39: exit status 255
ssh: connect to host 1.2.3.4 port 22: Operation timed out
again: main.go:39: exit status 255
ssh: connect to host 1.2.3.4 port 22: Operation timed out
Last login: Sat Dec  8 13:52:12 2018 from 5.6.7.8
marc@myserver:~$
```
