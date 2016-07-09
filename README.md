# rpmbuild-hatop

Create a hatop RPM for RHEL/CentOS.

## Requirements

To download package sources and install build dependencies

    yum -y install rpmdevtools yum-utils

## Build process

To build the package follow the steps outlined below

    git clone https://github.com/linuxhq/rpmbuild-hatop.git rpmbuild
    mkdir rpmbuild/SOURCES
    spectool -g -R rpmbuild/SPECS/hatop.spec
    yum-builddep rpmbuild/SPECS/hatop.spec
    rpmbuild -ba rpmbuild/SPECS/hatop.spec

## License

BSD

## Author Information

This package was created by [Taylor Kimball](http://www.linuxhq.org).
