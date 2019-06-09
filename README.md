# devsecops-app

This repository is for the use with DevSecOps training.

It is based on https://github.com/jenkins-docs/simple-java-maven-app

The repository contains a simple Java application which outputs the string
"Hello world!" and is accompanied by a couple of unit tests to check that the
main application works as expected. The results of these tests are saved to a
JUnit XML report.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline)
you'll be creating yourself during the tutorial and the `scripts` subdirectory
contains a shell script with commands that are executed when Jenkins processes
the "Deliver" stage of your Pipeline.

## Install Jenkins Container on Windows

* Open PowerShell, copy and paste the command below to install:
```
docker run `
  --rm `
  -u root `
  -p 8080:8080 `
  -v jenkins-data:/var/jenkins_home `
  -v /var/run/docker.sock:/var/run/docker.sock `
  -v $HOME`:/home `
  jenkinsci/blueocean
```

## Install Jenkins Container on Linux

* Open Terminal, copy and paste the command below to install:
```
sudo docker run \
--rm \
-u root \
-p 8080:8080 \
-v jenkins-data:/var/jenkins_home \
-v /var/run/docker.sock:/var/run/docker.sock \
-v "$HOME":/home \
jenkinsci/blueocean
```