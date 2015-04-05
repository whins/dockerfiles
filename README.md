# Dockerfiles

Repository contains Dockerfiles for different task.

## Install docker in Ubuntu

From https://docs.docker.com/installation/ubuntulinux/

    $ wget -qO- https://get.docker.com/ | sh

## Install docker in OSX

From https://docs.docker.com/installation/mac/

### Install Boot2Docker

1. Go to the [boot2docker/osx-installer](https://github.com/boot2docker/osx-installer/releases/latest) release page.
2. Download Boot2Docker by clicking Boot2Docker-x.x.x.pkg in the "Downloads" section.
3. Install Boot2Docker by double-clicking the package.

The installer places Boot2Docker in your "Applications" folder.

The installation places the docker and boot2docker binaries in your /usr/local/bin directory.

### From your command line

Initialize and run boot2docker from the command line, do the following:

1. Create a new Boot2Docker VM.

        $ boot2docker init

    This creates a new virtual machine. You only need to run this command once.

2. Start the boot2docker VM.

        $ boot2docker start

3. Display the environment variables for the Docker client.

        $ boot2docker shellinit
        Writing /Users/mary/.boot2docker/certs/boot2docker-vm/ca.pem
        Writing /Users/mary/.boot2docker/certs/boot2docker-vm/cert.pem
        Writing /Users/mary/.boot2docker/certs/boot2docker-vm/key.pem
            export DOCKER_HOST=tcp://192.168.59.103:2376
            export DOCKER_CERT_PATH=/Users/mary/.boot2docker/certs/boot2docker-vm
            export DOCKER_TLS_VERIFY=1

    The specific paths and address on your machine will be different.

4. To set the environment variables in your shell do the following:

        $ eval "$(boot2docker shellinit)"

    You can also set them manually by using the export commands boot2docker returns.

5. Run the hello-world container to verify your setup.

        $ docker run hello-world
