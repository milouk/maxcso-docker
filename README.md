This repository container a Dockerfile for running maxcso in Docker.

## How to use

Assuming we have an *.iso file in the directory `/home/user/desktop/my.iso`.
In order to use maxcso we first need to build the image using the following
command:

`docker build -t maxcso .`

We can then use `maxcso` as follows:

`docker run --rm -v "/home/user/desktop":/desktop -w /desktop/ maxcso maxcso --block=2048 --format=zso my.iso`
