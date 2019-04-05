demo jenkin docker
install notifical in slack
https://www.youtube.com/watch?v=TWwvxn2-J7E

config: build with parameters chose branch in git
install: plugin git parameter
https://wiki.jenkins.io/display/JENKINS/Git+Parameter+Plugin

https://medium.com/@schogini/running-docker-inside-and-outside-of-a-jenkins-container-along-with-docker-compose-a-tiny-c908c21557aa
https://oncomputingwell.princeton.edu/2018/01/triggering-a-jenkins-build-every-time-changes-are-pushed-to-a-git-branch-on-github/

Note: khi cai dat cac service (nginx, php-fpm, mysql) trong docker jenkins thi phai dong bo socket service jenkin voi cac service nay
/var/run/docker.sock:/var/run/docker.sock  # Expose the docker daemon in the container
https://code-maze.com/ci-jenkins-docker/