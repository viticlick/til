#  Run jshell with docker
If you want to execute jshell in your system but you don't have the newest jdks in your machine, you can use docker to solve this problem.
First download one jdk image from docker registry.

```bash
 ~$ docker pull openjdk:9-jdk
```

And next, run the jshell in docker

```bash
 ~$ docker run --rm -ti openjdk:9-jdk /bin/jshell -v
```
