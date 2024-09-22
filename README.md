# Project2-Compose
Repository to to store the Docker Compose configuration and related files for running Jenkins.

Run `docker compose up` command to run the DinD container.</br></br>
run `docker container run --name jenkins --detach --restart unless-stopped --network jenkins -u root --env DOCKER_HOST="tcp://docker:2376" --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1 --volume docker-certs-client:/certs/client:ro --volume jenkins-data:/var/jenkins_home --publish 8080:8080 --publish 50000:50000 -v /usr/bin/docker:/usr/bin/docker jenkins/jenkins:lts-jdk11` command to start Jenkins container that uses the DinD container to run a Jenkins pipeline.</br>
</br>
Setup Jenkins using initial admin password: `docker logs jenkins `
</br>
</br>
Jenkins can be opened on 0.0.0.0:8000 port can follow the instructions to log in and install the plugins.</br>
</br>

Plugins to be installed are:</br>
`Docker,
Docker Pipeline,
Git`
