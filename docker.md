# Docker

## Resources
  - [Docker Ecosystem Map]( https://www.mindmeister.com/389671722/docker-ecosystem)
  - [Docker Hub](https://hub.docker.com/)

## Commands
### docker-machine
  - Get Docker Machine IP
  ```
  $ docker-machine ip
  $ docker-machine ip <NAME-OF-MACHINE> (ie. default)
  # get the ip address docker machine is running on
  ```

  - Create Linux VM
  ```
  $ docker-machine create --driver virtualbox default
  # create the Linux VM which will hold the docker daemon if it doesn't already exist
  # also creates machine configuration in ~/.docker/machine/machines/default )
  ```

  - List VMs
  ```
  $ docker-machine ls
  # list machines, or open virtualbox to see
  ```

  - Get variables, connect shell to machine
  ```
  $ docker-machine env default
  $ /usr/local/bin/docker-machine env default
  # To see how to connect your Docker Client to the Docker Engine running on this virtual machine
  ```

  - Remove machine
  ```
  $ docker-machine rm <machine-name>
  # remove <machine-name> linux vm, ie. 'default'
  ```

### docker
  - Run Image
  ```
  $ docker run <name-of-image>
  # run a local docker image
  -
  $ docker run <hub-username>/<name-of-image>
  # run a docker image tagged to repo
  ```

  - Show Images
  ```
  $ docker images
  # show docker images on local
  ```

  - Login Hub
  ```
  $ docker login --username=yourhubusername --email=youremail@company.com
  # to log in to hub, followed by pass prompt
  ```

  - Tag
  ```
  $ docker tag <image-id> <hub-username>/<image-name>:latest
  # to tag an image ie. associate it with repo on hub account
  ```

  - Login 3rd party hub
  ```
  $ docker login --email=<EMAIL> --username=<USERNAME> --password=<GENERATED-PASS> docker.<REST-OF-URL>
  ```

### Notes
  - Build = the build parameters
  - Context = Either a path to a directory containing a Dockerfile, or a url to a git repository.
  - Dockerfile = Compose will use an alternate file to build with. A build path must also be specified.
  - Args = build arguments as key values pairs.
  - Command = Override the default command (command: bundle exec thin -p 3000). The command can also be a list, in a manner similar to dockerfile(command: [bundle, exec, thin, -p, 3000]):
  - Environment = Add environment variables as kvp's.
  - Expose  = Expose ports without publishing them to the host machine - they’ll only be accessible to linked services. Only the internal port can be specified.
  - Image = Tag or partial image ID. Can be local or remote - Compose will attempt to pull if it doesn’t exist locally.
  - Links = Link to containers in another service. Either specify both the service name and a link alias (SERVICE:ALIAS), or just the service name.
  - Volumes = Mount paths or named volumes, optionally specifying a path on the host machine (HOST:CONTAINER), or an access mode (HOST:CONTAINER:ro) Restart = always, on-failure,etc.
  - Ports: When mapping ports in the HOST:CONTAINER format, you may experience erroneous results when using a container port lower than 60, because YAML will parse numbers in the format xx:yy as sexagesimal (base 60). For this reason, we recommend always explicitly specifying your port mappings as strings.
