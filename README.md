# Docker Compose Subordinate

This charm enables you to deploy a docker-compose based formation, out of any
arbitrary GIT repository.

## Usage

Ensure you have a docker-cluster running complete with the registrator charm:

    juju deploy docker
    juju deploy registrator
    juju deploy consul
    juju deploy nginx-proxy
    juju add-relation registrator docker
    juju add-relation registrator:api consul:api
    juju add-relation nginx-proxy:template consul:api

Using the example of deploying the 2048 HTML5 game running in a docker container:

    juju deploy docker-compose twenty-fourty-eight
    juju set twentry-fourty-eight repository=https://github.com/chuckbutler/docker-demos.git path=2048
    juju add-relation twenty-fourty-eight docker

## Known Limitations and Issues

This not only helps users but gives people a place to start if they want to help you add features to your charm.

# Configuration

[todo]

# Contact Information

[todo]

