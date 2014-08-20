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

