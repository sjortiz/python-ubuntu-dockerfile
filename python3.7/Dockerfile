# python 3.7 ubuntu based image
FROM ubuntu:16.04

# apt-get and system utilities
RUN apt-get update && apt-get install -y \
    curl \
    apt-utils\
    apt-transport-https\
    debconf-utils\
    gcc\
    build-essential\
    g++-5\
    && rm -rf /var/lib/apt/lists/*

# python libraries
RUN apt-get install -y software-properties-common
RUN add-apt-repository ppa:deadsnakes/ppa
RUN apt-get update

RUN apt-get install -y\
    build-essential\
    python3.7\
    python3.7-dev\
    python3-pip\
    python3.7-venv

# update pip
RUN python3.7 -m pip install pip --upgrade
# Installing wheel to extend the compiler
RUN python3.7 -m pip install wheel
# Creating alias to be able to execute pip in the short way
RUN alias pip="python3.7 -m pip"
# Default commant to python 3.7
CMD ["python3.7"]
