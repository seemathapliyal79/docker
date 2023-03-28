When you use a bind mount, a file or directory on the host machine is mounted into a container. 
The file or directory is referenced by its absolute path on the host machine. 
By contrast, when you use a volume, a new directory is created within Docker’s storage directory on the host machine, and Docker manages that directory’s contents.

-v or --volume: Consists of three fields, separated by colon characters (:)... <src>:<dst>.. src is file or directory on host and dst is inside container
docker run -d -P --volume /opt/nginxlogs:/var/log/nginx -v /opt/nginxconf:/usr/share/nginx/html nginx:latest

--mount: Consists of multiple key-value pairs, separated by commas and each consisting of a <key>=<value> tuple
docker run -d   -it   --name tmptest   --mount type=tmpfs,destination=/app   nginx:latest
  
      Differences between -v and --mount behavior
If you use -v or --volume to bind-mount a file or directory that does not yet exist on the Docker host, -v creates the endpoint for you. It is always created as a directory.
If you use --mount to bind-mount a file or directory that does not yet exist on the Docker host, Docker does not automatically create it for you, but generates an error.
  
 
 
