# Docker rpmbuild #

This RPM contains a few docker containers used to build RPMs. It gives you a fully portable build environment.

For a fairly standard RPM building container, there is `github-cent*`.

For more in depth containers designed for a specific build system, there is `sysops-cent*`.


## Github builds ##
To be used for building RPMs that are just a git repository

### Github CentOS 6 ###
Build from root of this repo with:
```
docker build -t jakdept/rpmbuild:cent6 github-cent6
```

Run from the root of the build repository with:

```
docker run -i -t --rm -v $(pwd)/:/home/rpmbuild/package jakdept/rpmbuild:cent6
```

## Github CentOS 7 ##
Build from the root of this repository with:
```
docker build -t jakdept/rpmbuild:cent7 github-cent7
```

Run from the root of the build repository with:
```
docker run -i -t --rm -v $(pwd)/:/home/rpmbuild/package jakdept/rpmbuild:cent7
```

## Sysops builds ##
To be used to test building rpms from SysOps's repository

### Sysops CentOS 6 ###
Build from root of this repo with:
```
docker build -t jakdept/rpmbuild-ops:cent6 sysops-cent6
```

Run from the root of the sysops repository with:
```
docker run -i -t --rm -v $(pwd):/home/rpmbuild/packages jakdept/rpmbuild-ops:cent6
```

### Sysops CentOS 7 ###
Build from root of this repo with:
```
docker build -t jakdept/rpmbuild-ops:cent7 sysops-cent7
```

Run from the root of the sysops repository with:
```
docker run -i -t --rm -v $(pwd):/home/rpmbuild/packages jakdept/rpmbuild-ops:cent7
```
