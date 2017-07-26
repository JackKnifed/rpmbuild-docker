## RPM build syntax

FROM centos:7
MAINTAINER Jack Hayhurst <jhayhurst@liquidweb.com>

RUN adduser -u 1000 rpmbuild

# install build tools
RUN yum install -y \
			rpm-build \
			git \
			make \
			gcc \
			zsh

VOLUME "/home/rpmbuild/packages"

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc && \
			chsh -s /bin/zsh

RUN		chsh -s /bin/zsh rpmbuild

USER rpmbuild
WORKDIR /home/rpmbuild

RUN echo '%_topdir    /home/rpmbuild/packages/rpmbuild' >> /home/rpmbuild/.rpmmacros

RUN mkdir -p /home/rpmbuild/packages

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

# enter as zsh
CMD /bin/zsh
