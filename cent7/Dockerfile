## RPM build syntax

FROM centos:7
MAINTAINER Jack Hayhurst <jhayhurst@liquidweb.com>

# install build tools
RUN yum install -y \
			rpm-build \
			git \
			make \
			gcc \
			zsh

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc && \
			chsh -s /bin/zsh

RUN mkdir -p /root/rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}

WORKDIR /root

# enter as zsh
CMD /bin/zsh
