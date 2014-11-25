## Docker

```bash
$ cd jnst-devops/docker/jenkins
$ docker build -t jnst/jenkins:latest
$ docker run --name=jenkins -d -p 8080:8080 jnst/jenkins
$ open http://$(boot2docker ip 2>/dev/null):8080
```
