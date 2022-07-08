# Requirments
Docker and docker-compose are required for this build.

# Supported Platforms
This should work on any linux based x86_64 architecture. It has been build and tested on MacOS x86_64. 
Arm platform, including Mac M1 are *`not supported`*

# Description 
Run your own nodeos for testing/prototyping. Takes the latest (3.0+) release of mandel mandel.cdt and mandel-contract and puts them in a docker container. Build off [EOS Network Foundation repositories](https://https://github.com/eosnetworkfoundation)

# Installation

Steps to install. 

## `Build`
Run the build script, which is a simple wrapper on docker-compose
```console
$ ./scripts/build.sh
```

Behind the scenes this will build the Docker Image using *Dockerfile*. It runs a bootstrap which copies down the mandel 3.0 binary releases. It starts up nodeos.

## `Run Container`
Run the container script, which is a wrapper on docker
```console
$ ./scripts/run.sh
```

Behind the scenes this will run docker opening up the required ports, and if specificed mount a shared volume between host and docker container.

## `Validating`
Run the validation script, which tests the setup to make sure things are working as expected
```console
$ ./scripts/validate.sh
```

Behind the scenes this will test for open ports. 
