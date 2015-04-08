# Docker recipe for [mongo](https://github.com/mongodb/mongo)

See the global picture how this container interacts with other components to run Dogeparty:

[Global Component Overview](http://www.inkpad.io/1GMXYwxl4Q)


## Instantiate Data Container

### Mainnet

    docker run -d --name=mongo-data mongo:latest bash


### Testnet

    docker run -d --name=mongo-testnet-data mongo:latest bash


## Run Container

### Mainnet

    docker run -it --name mongo --volumes-from=mongo-data mongo:latest bash


### Testnet

    docker run -it --name mongo-testnet --volumes-from=mongo-testnet-data mongo:latest bash


## Run Process

    mongod


## Backup

    mongodump  --db counterblockd --out dogeblockd-$(date +%y-%m-%d-%H:%M)

