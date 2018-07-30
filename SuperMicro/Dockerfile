## RPM build syntax

FROM centos:7
LABEL maintainer "Jack Hayhurst <jakdept@gmail.com>"

RUN adduser -u 1000 sum

WORKDIR /home/sum
COPY sum_2.0.1_Linux_x86_64*.tar.gz /home/sum/
RUN tar -xzvf sum_2.0.1_Linux_x86_64*.tar.gz

RUN cp /home/sum/sum_*/sum /usr/bin/

RUN chown -R sum. /home/sum

USER sum

VOLUME "/home/sum/Downloads"

CMD /bin/bash
