.PHONY: build cluster test

default: build

build:
	go build -o bin/swarm    github.com/panghalamit/go-ethereum/cmd/swarm
	go build -o bin/geth     github.com/panghalamit/go-ethereum/cmd/geth
	go build -o bin/bootnode github.com/panghalamit/go-ethereum/cmd/bootnode

cluster: build
	scripts/boot-cluster.sh

test:
	go test -v github.com/panghalamit/go-ethereum/swarm/...
