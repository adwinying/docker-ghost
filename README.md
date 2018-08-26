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

3. Configure your ghost install. Under `ghost` in `docker-compose.yml`:
```yaml
ghost:
  environment:
    # your blog URL
    - url=https://blog.example.com
    # host config for nginx
    - VIRTUAL_HOST=blog.example.com
    # host config for Let's Encrypt SSL
    - LETSENCRYPT_HOST=blog.example.com
    # in case of cert renewal fails, let's encrypt will email you
    - LETSENCRYPT_EMAIL=admin@example.com
```

4. Set up the docker image
```bash
# -d to run containers in detached mode
$ docker-compose up -d
```

5. Navigate to the host URL you defined in the `docker-compose.yml` file and if you see the ghost blog, you're good to go!
