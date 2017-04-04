
### required directories ###

```
mkdir RPMS SRPMS SPECS SOURCES
```
To be used to test building RPMS on CentOS 7

## CentOS 5
### build in cwd with ###
```
docker build -t jakdept/rpmbuild:cent5 cent5
```

### run with ###
```
docker run -i -t --rm \
 -v $(pwd)/:/root/ \
 -v $(pwd)/RPMS/:/root/rpmbuild/RPMS \
 -v $(pwd)/SRPMS/:/root/rpmbuild/SRPMS \
 -v $(pwd)/SPECS/:/root/rpmbuild/SPECS \
 -v $(pwd)/SOURCES/:/root/rpmbuild/SOURCES \
 jakdept/rpmbuild:cent5
```

## CentOS 6
### build in cwd with ###
```
docker build -t jakdept/rpmbuild:cent6 cent6
```

### run with ###
```
docker run -i -t --rm \
 -v $(pwd)/:/root/ \
 -v $(pwd)/RPMS/:/root/rpmbuild/RPMS \
 -v $(pwd)/SRPMS/:/root/rpmbuild/SRPMS \
 -v $(pwd)/SPECS/:/root/rpmbuild/SPECS \
 -v $(pwd)/SOURCES/:/root/rpmbuild/SOURCES \
 jakdept/rpmbuild:cent6
```

## CentOS 7 ##
### build in cwd with ###
```
docker build -t jakdept/rpmbuild:cent7 cent7
```

### run with ###
```
docker run -i -t --rm \
 -v $(pwd)/:/root/ \
 -v $(pwd)/RPMS/:/root/rpmbuild/RPMS \
 -v $(pwd)/SRPMS/:/root/rpmbuild/SRPMS \
 -v $(pwd)/SPECS/:/root/rpmbuild/SPECS \
 -v $(pwd)/SOURCES/:/root/rpmbuild/SOURCES \
 jakdept/rpmbuild:cent7
```
