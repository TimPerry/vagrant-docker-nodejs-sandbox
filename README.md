# vagrant-docker-nodejs-sandbox

# Overview

A simple vagrant, docker setup to host a nodejs app. I created this as I wanted a simplistic example, hopefully it will be useful to others.

# Install

- Clone this repo
- Make sure you have vagrant installed
- Change into the repos directory

Install the docker-compose plugin:
```
vagrant plugin install vagrant-docker-compose
```

Start up vagrant:
```
vagrant up
```

# Run the specs

This will run the specs on the sandbox in a docker container

```
bundle install # only needed the first time 
rake spec
```