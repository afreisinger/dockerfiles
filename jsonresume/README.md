# README

This container makes it easy for you to create, render and publish your [JSON based resume](https://jsonresume.org/).

## To build:
```
docker build -t afreisinger/jsonresume:latest .
```

## To build and push:
```
docker buildx build -t afreisinger/jsonresume:latest --push .
```



## To run:
```
docker run -it \
        --user root \
        --workdir /home/pptruser \
        -v $(pwd):/home/pptruser afreisinger/jsonresume:latest resume init
```
Then, enter your name and Email address. Note that you can mask your email address for preventing spammer to find that. (e.g mail [AT] domain dot com).
Remember this file was created as the root user. so you need to do:
```
sudo chown -R $USER resume.json
```
Now open the resume.json and fill the file with your contact information, your skills, your social networks, and your job experiences.

## To test
```
docker run -it  \
        --user root \
        --workdir /home/pptruser \
        -v $(pwd):/home/pptruser afreisinger/jsonresume:latest resume export resume.html -f html --theme flat
```
You can export to pdf simply by changing the extension.

## Setup CI

Check the [repo](https://gitlab.com/afreisinger/afreisinger.gitlab.io) of the project and take a look at the .gitlab-ci.yml file, Dockerfile, and resume.json file. That’s it.

## Resume
My [resume](https://afreisinger.gitlab.io/) is ready from Gitlab.