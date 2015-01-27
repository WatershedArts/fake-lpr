# Fake LPR

## Description

RPM to "provide" `/bin/lp` and `/bin/lpr` to satisfy the dependency requirements of the `redhat-lsb-core` package without needing to install CUPS and X11.

## For more information:

Please visit our [blog post](http://blogs.wcode.org/2015/01/fake-lpr-or-how-to-install-redhat-lsb-core-without-cups-and-x11/).

## Building

1. We're assuming you're on a CentOS box
2. Start by installing the pre-requisites:
```
yum install rpm-build
```
3. Download the `fake-lpr.spec` file in this repo.
4. Build the package:
```
rpmbuild -ba fake-lpr.spec
```

## Installation

1. Deploy the generated RPM, or grab a the prebuilt one in this repo.
2. Install it with:
```
sudo rpm -ivh fake-lpr-1.0-1.noarch.rpm
```