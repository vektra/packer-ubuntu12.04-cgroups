# Packer Template for Ubuntu 12.04 and CGroups

This repository contains a Packer template for building machine images
that are have a modern 3.x kernel and thus have cgroups fully available.

Contains providiors for virtualbox, vmware, and amazon.

## Usage

First, [install Packer](http://www.packer.io/intro/getting-started/setup.html).
Then, clone this repository and `cd` into it.

Run the following:

```
$ export AWS_ACCESS_KEY="your aws access key"
$ export AWS_SECRET_KEY="your aws secret key"
$ packer build template.json
```

This will build them all, to just build virtualbox
```
$ packer build -only=virtualbox-iso template.json
```

