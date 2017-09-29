## Python Tornado web framework Docker image.

### Description:

Python Tornado web framework Docker image for development purposes.
Based on ubuntu:16.04 with a mount point, runs python 3.5, 
on build fetches latest Tornado version with pip, listens on port 8888.

### Usage:

- volume: /usr/app
- exposed port: 8888
- environment variables:
    ENTRY

ENTRY variable is optional and can be used to setup starting python script.
By default it is "index.py", so volume should contain python script named index.py 
if another is not specified.

### Usage samples:

$ docker run --name docker-tornado -p 8888:8888 -v /path/to/src:/usr/app warg/docker-tornado

$ docker run --name docker-tornado -p 8888:8888 -v /path/to/src:/usr/app -e "ENTRY=entry.py" warg/docker-tornado
