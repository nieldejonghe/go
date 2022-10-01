# go
repository to keeping track of notes and projects while learning go also called golang

# 1. Introduction to GO
Following this youtube video:
https://www.youtube.com/watch?v=yyUHQIec83I

Goal of the video is to write a simple CLI app to learn the core concepts and syntax of go.

# Why go?
Designed to run on multiple cores and built to support concurrency (Doing more than one thing at the same time)
                                                                                                                               
# Setting up your local env to work with go

Downloading latest version of go with cli

# find latest version using curl or by manually looking at download page
VERSION=$(curl -s https://go.googlesource.com/go | grep -Po "<li class=\"RefList-item\"><a href=\"/go/\+/refs/tags/go\d\.\d*\">go\K(\d\.\d*)</a></li>" | cut -d'<' -f1)

curl -O -L "https://golang.org/dl/go${VERSION}.linux-amd64.tar.gz"

# Note we are not untarring the archive into an existing /usr/local/go tree as this is known to produce broken Go installations
sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go${VERSION}.linux-amd64.tar.gz

# FYI: With the PATH variable, you tell the Operating System where to look in order to start a program, 
# and the environmental variable is the place where the Operating System expects this kind of information.
export PATH=$PATH:/usr/local/go/bin
go version


