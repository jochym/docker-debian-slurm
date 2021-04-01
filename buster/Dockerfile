FROM debian:buster-slim
LABEL maintainer="Paweł T. Jochym <jochym@wolf.ifj.edu.pl>"

# Set correct environment variables.
ENV HOME /root
ENV DEBIAN_FRONTEND noninteractive
ENV LC_ALL C.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US.UTF-8

RUN apt-get update -q && \
    apt-get -y full-upgrade && \
    apt-get -y install locales

# Install locales
RUN locale-gen en_US.UTF-8



ENV BUILD_DEPS="git devscripts equivs apt-utils apache2-dev libslurm-dev python-setuptools cython python-dev slurm-wlm-basic-plugins-dev libslurmdb-dev ca-certificates"

ENV RUN_DEPS="apache2 libapache2-mod-wsgi javascript-common python-flask clustershell libjs-bootstrap libjs-jquery-flot libjs-jquery-tablesorter munge slurm-wlm node-uglify fonts-dejavu-core python-ldap python-redis libjs-requirejs libjs-requirejs-text libjs-three libjs-d3 libjs-handlebars libjs-async python-clustershell"


# Install system dependencies
RUN apt-get -y install libslurm-dev libslurmdb-dev cython python-dev python3-dev python-setuptools python3-setuptools slurm-wlm

# Cleanup
RUN apt-get clean 

