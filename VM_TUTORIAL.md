start your docker darmon 

- boot:
    docker-machine start dev
- check your ip
    docker-machine ip dev

pull the docker image from the dockerhub

    docker pull sequenceiq/hadoop-docker:2.7.1

connect to a machine 

    docker exec -ti apachesparkplayground_master_1 zsh

upgrad docker-machine

    docker-machine upgrade default    