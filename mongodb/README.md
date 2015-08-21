# Dockerfile for MongoDB


## Basic usage

### Create image from Dockerfile

```bash
$ docker build .
```

or

```bash
$ docker build -t <your_tag> .
```

### Running

```bash
$ docker run -p 27017:27017 -d <image_id>
```

```bash
$ docker run -p 27017:27017 -d <your_tag>
```

### How to test

```bash
$ nc -zvv localhost 27017
```

if you use `boot2docker` on mac or `docker-machine`, you should do:

```bash
$ boot2docker ip
```
or

```bash
$ docker-machine ip <machine_name>
```
and

```bash
$ nc -zvv <machine_ip> 27017
```
