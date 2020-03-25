#!/bin/bash
    tty=
    tty -s && tty=--tty
    docker run \
        $tty \
        --interactive \
        --rm \
        --net=host \
        --user $(id -u):$(id -g) \
        --volume /etc/passwd:/etc/passwd:ro \
        --volume /etc/group:/etc/group:ro \
        --volume /tmp:/tmp \
        --volume $(pwd):/app \
        donglf681/composer:1.10.1 "$@"
