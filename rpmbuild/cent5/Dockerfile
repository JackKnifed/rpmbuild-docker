## RPM build syntax

FROM centos:5
MAINTAINER Jack Hayhurst <jhayhurst@liquidweb.com>

ENV PATH ~/bin:$PATH

# install build tools
RUN yum install -y \
			rpm-build \
			make \
			gcc \
			zlib-devel \
			openssl-devel \
			cpio \
			expat-devel \
			gettext-devel \
			curl \
			curl-devel \
			zsh


WORKDIR /usr/local/src
RUN curl http://layer3.liquidweb.com/scripts/plBake/packages/git/git-1.8.3.4.tar.gz | tar xz

WORKDIR /usr/local/src/git-1.8.3.4
RUN make && make install

# install zshrc
RUN git clone git://github.com/robbyrussell/oh-my-zsh.git /root/.oh-my-zsh && \
			cp /root/.oh-my-zsh/templates/zshrc.zsh-template /root/.zshrc && \
			chsh -s /bin/zsh

RUN mkdir -p /root/rpmbuild/{BUILD,RPMS,SOURCES,SPECS,SRPMS}

# enter as zsh
CMD /bin/zsh
