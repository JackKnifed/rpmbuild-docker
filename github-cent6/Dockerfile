## RPM build syntax

FROM centos:6
LABEL maintainer "Jack Hayhurst <jakdept@gmail.com>"

RUN adduser -u1000 rpmbuild

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

RUN mkdir -p /home/rpmbuild

RUN echo '%_topdir    /home/rpmbuild/packages' >> /home/rpmbuild/.rpmmacros

# RUN ln -s /home/rpmbuild/package /home/rpmbuild/SPECS
# RUN ln -s /home/rpmbuild/package /home/rpmbuild/SOURCES
# RUN ln -s /home/rpmbuild/package /home/rpmbuild/RPMS

COPY gitconfig /home/rpmbuild/.gitconfig
COPY gitignore /home/rpmbuild/.gitignore

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh && \
			cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

# enter as zsh
CMD /bin/zsh
