FROM phusion/baseimage:0.9.18

MAINTAINER Anson Hu<huhuan2048@gmail.com>

# Use baseimage-docker's init system.
CMD ["/sbin/my_init"]

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN apt-get update && apt-get upgrade -y -o Dpkg::Options::="--force-confold"

