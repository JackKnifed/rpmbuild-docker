## RPM build syntax

FROM centos:7
LABEL maintainer "Jack Hayhurst <jakdept@gmail.com>"

RUN adduser -u 1000 rpmbuild

# install build tools
RUN yum install -y \
			rpm-build \
			git \
			make \
			gcc \
			zsh

VOLUME "/home/rpmbuild/package"

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc && \
			chsh -s /bin/zsh

RUN		chsh -s /bin/zsh rpmbuild

USER rpmbuild
WORKDIR /home/rpmbuild

RUN mkdir -p /home/rpmbuild

RUN ln -s /home/rpmbuild/package /home/rpmbuild/SPECS
RUN ln -s /home/rpmbuild/package /home/rpmbuild/SOURCES
RUN ln -s /home/rpmbuild/package /home/rpmbuild/RPMS

RUN echo '%_topdir    /home/rpmbuild' >> /home/rpmbuild/.rpmmacros

COPY gitignore /home/rpmbuild/.gitignore

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

# enter as zsh
CMD /bin/zsh
