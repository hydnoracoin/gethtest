.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/hydnoracoin/node/cmd/swarm
	go build -o bin/geth     github.com/hydnoracoin/node/cmd/geth
	go build -o bin/bootnode github.com/hydnoracoin/node/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/hydnoracoin/node/swarm/...
