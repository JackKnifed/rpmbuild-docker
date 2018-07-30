## RPM build syntax

FROM centos:7
LABEL maintainer "Jack Hayhurst <jakdept@gmail.com>"

RUN adduser -u 1000 sum

# install build tools
RUN yum install -y \
	git \
	make \
	gcc \
	tar

VOLUME "/home/sum"

USER sum
WORKDIR /home/sum

# you have to manually copy the .zip from supermicro for linux into this folder
COPY sum_2.0.1_Linux_x86_64*.tar.gz /home/sum/

RUN tar xvfz /home/sum/sum_2.0.1_Linux_x86_64*.tar.gz

CMD /bin/bash
