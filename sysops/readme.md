
### required directories ###

To be used to test building RPMS from sysops's repository

## CentOS 6
### build in cwd with ###
```
docker build -t jakdept/rpmbuild:ops-cent6 cent6
```

### run with ###
```
docker run -i -t --rm \
 -v $(pwd) \
 jakdept/rpmbuild:ops-cent6
```

## CentOS 7 ##
### build in cwd with ###
```
docker build -t jakdept/rpmbuild:ops-cent7 cent7
```

### run with ###
```
docker run -i -t --rm \
 -v $(pwd) \
 jakdept/rpmbuild:ops-cent7
```
