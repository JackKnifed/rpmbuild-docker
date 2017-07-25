
To be used for building RPMs that are just a git repository

## CentOS 6
### build in cwd with ###
```
docker build -t jakdept/rpmbuild:cent6 cent6
```

### run with ###
```
docker run -i -t --rm \
 -v $(pwd)/:/home/rpmbuild/package \
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
 -v $(pwd)/:/home/rpmbuild/package \
 jakdept/rpmbuild:cent7
```
