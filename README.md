# Docker Python sandbox

This is a fork of [christophetd/docker-python-sandbox](https://github.com/christophetd/docker-python-sandbox).

## Changes
- To support Docker on Mac, exposed ports on Docker instances (specifically the :3000 port which receives the Python code to be executed) are published on the host machine to a random other port. This library then accesses the container via a URL like "localhost:32456" instead of the container directly such as "127.17.0.1" This fixes an issue where the library would not work on Mac: see [this](https://github.com/christophetd/docker-python-sandbox/issues/14) and [this](https://stackoverflow.com/questions/45390579/docker-for-mac-cant-curl-my-container) for more context.