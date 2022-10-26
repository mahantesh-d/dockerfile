Dockerfile

Special instruction for using the docker file 'StandaloneHadoop'
1. port 9870 -->> For namenode web UI interface, expose the port
2. port 8088 -->> For yarnmanager, expose the port
3. Use the docker hostname as hadoop as same is configured in core-site.xml

Example: 
docker run -P --privileged -d -ti -e "container=docker" -v /sys/fs/cgroup:/sys/fs/cgroup --name hadoop -h hadoop -p 9870:9870 -p 8088:8088 <image-id> /usr/sbin/init

above is the docker command to start the container with hostname as 'hadoop' and both ports are exposed

