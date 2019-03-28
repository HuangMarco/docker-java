#  json conf can’t override the systemd one 
According to the official documen, we can add /etc/docker/daemon.json to override the system one. But actually this is a bug.

<br>
You are not able to restart the docker serivce once you add that json file.
<br>
Workaround as here:https://forums.docker.com/t/failed-to-start-docker-application-container-engine/35594