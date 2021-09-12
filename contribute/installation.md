# Installation
## Introduction
If you've ever used Docker before, running Arken is as simple as pulling and configuring
a new docker container. If you haven't used docker before, no worries, we'll walk you
through it!

First you'll need an old computer or home server that's got at least 5 Gigabytes of space
free and can run Linux. (Although Linux is not required to run Arken, it's what we're going
to be covering in this article. For more information on running Docker containers on Windows
check out the link [here](https://docs.docker.com/docker-for-windows/).

## Installing Docker
### Step 1: Installing Docker on Your Machine
Once you've got your machine up and running, we'll need to install docker to deploy & manage the Arken container. Depending on the distribution of Linux your running on your local machine the instructions for installing docker might vary slightly. In this article we're going to focus on installing Docker on a machine running Debian. So if you're running a different form of Linux we recommend you look at the specific instructions for your distribution [here](https://docs.docker.com/engine/install/).

### Step 2: Configuring the Docker Repo
```bash
$ sudo apt-get update

$ sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

$ curl -fsSL https://download.docker.com/linux/debian/gpg | sudo apt-key add -

$ sudo add-apt-repository \
    "deb [arch=amd64] https://download.docker.com/linux/debian \
    $(lsb_release -cs) \
    stable"
```

### Step 3: Install the Docker Container Engine
```bash
$ sudo apt-get update
$ sudo apt-get install docker-ce docker-ce-cli containerd.io
```

### Step 4: Enable Docker to Start When the Computer Does
```bash
$ sudo systemctl enable --now docker
```

### Step 5: Installing Docker-Compose
Docker-Compose is a tool in the family of docker applications that allows us to easily define a group of docker containers and how we want to configure them. You can learn more about docker-compose [here](https://docs.docker.com/compose/).

```bash
$ sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)"\-o /usr/local/bin/docker-compose

$ sudo chmod +x /usr/local/bin/docker-compose

$ sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
```

## Installing Arken
Now that you've got Docker and Docker-Compose up and running on your computer it's time for the fun part. Let's first define our docker-compose configuration file. Put this file anywhere you want and have easy access to.

Run the following to download a template Arken Config File,
```bash
wget https://raw.githubusercontent.com/arken/arken/main/docs/examples/docker-compose.yml
```

Now you can open that file by typing,
```bash
nano docker-compose.yml
```

Read through this file and change all of the fields with the < and > markers.

Once you are finished updating the file you can save your changes by pressing CTRL + X.
Now we can launch the docker containers by running,
```bash
sudo docker-compose up -d
```

**And that's it!** Arken is now running on your local machine! If you'd like to see the status of the application you can type,
```bash
sudo docker-compose logs -f arken
```
