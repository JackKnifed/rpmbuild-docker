
### required directories ###

```
mkdir -p working/rpmbuild/{rpms,specs,sources}
```
To be used to test building RPMS on CentOS 7

## CentOS 6 ## 
### build in cwd with ###
```
docker build -t jackknifed/rpmbuild:cent5 rpmbuild.cent5.dockerfile
```

### run with ###
```
docker run -i -t --rm jackknifed/rpmbuild:cent5 \
 -v ~/working/rpmbuild/rpms/:/root/rpmbuild/RPMS 
 -v ~/working/rpmbuild/specs/:/root/rpmbuild/SPECS 
 -v ~/working/rpmbuild/sources/:/root/rpmbuild/SOURCES
```

## CentOS 6 ## 
### build in cwd with ###
```
docker build -t jackknifed/rpmbuild:cent6 rpmbuild.cent6.dockerfile
```

### run with ###
```
docker run -i -t --rm jackknifed/rpmbuild:cent6 \
 -v ~/working/rpmbuild/rpms/:/root/rpmbuild/RPMS 
 -v ~/working/rpmbuild/specs/:/root/rpmbuild/SPECS 
 -v ~/working/rpmbuild/sources/:/root/rpmbuild/SOURCES
```

## CentOS 7 ##
### build in cwd with ###
```
docker build -t jackknifed/rpmbuild:cent7 rpmbuild.cent7.dockerfile
```

### run with ###
```
docker run -i -t --rm jackknifed/rpmbuild:cent7 \
 -v ~/working/rpmbuild/rpms/:/root/rpmbuild/RPMS 
 -v ~/working/rpmbuild/specs/:/root/rpmbuild/SPECS 
 -v ~/working/rpmbuild/sources/:/root/rpmbuild/SOURCES
```
