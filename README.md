A docker image with confd 6.6 installed on ubuntu 18.10

docker build -t docker-confd .

docker run --rm --name=confd -d -v ~/CENX/cenx-descriptors:/var/cenx-descriptors docker-confd

docker exec -it confd bash

docker stop confd

----
to publish
docker images
docker tag c12cbedbacd0 sprudhom/docker-confd:first
docker tag c12cbedbacd0 sprudhom/docker-confd:latest

docker push sprudhom/docker-confd

run from docker-hub
docker run --rm --name=confd -d -v ~/CENX/cenx-descriptors:/var/cenx-descriptors sprudhom/docker-confd


built from this example: https://docs.docker.com/get-started/part2/#build-the-app
# docker-confd
