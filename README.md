# docker-ghost
Personalized ghost setup running on docker

## Installation
0. Install docker CE and ensure it works by running
```bash
$ docker -v
$ docker-compose -v
```

1. Clone this repo
```bash
$ git clone https://github.com/adwinying/docker-ghost
```

2. If you have an existing docker install, copy the `content` folder to the directory root, else skip this step
```bash
$ cd docker-ghost
$ cp /path/to/content/folder ./
```

3. Set up the docker image
```bash
# -d to run containers in detached mode
$ docker-compose up -d
```

4. Navigate to [http://localhost:3001](http://localhost:3001) and if you see the ghost blog, you're good to go!
