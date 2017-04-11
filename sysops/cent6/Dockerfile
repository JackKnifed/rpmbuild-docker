## RPM build syntax

FROM centos:6
MAINTAINER Jack Hayhurst <jhayhurst@liquidweb.com>

RUN adduser rpmbuild

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

USER rpmbuild
WORKDIR /home/rpmbuild

RUN mkdir -p /home/rpmbuild/packages

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc && \
			chsh -s /bin/zsh

# enter as zsh
CMD /bin/zsh
