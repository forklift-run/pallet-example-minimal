# pallet-example-minimal
A simple "hello-world" Forklift pallet illustrating a minimal pallet structure

## Introduction

pallet-example-minimal is a [Forklift](https://github.com/PlanktoScope/forklift) pallet
specifying an example set of Forklift packages and package deployments.

## Usage

### Deployment

You can clone the latest commit of this Forklift pallet to a computer acting as a Docker host, by
using the [`forklift`](https://github.com/PlanktoScope/forklift) tool:
```
forklift plt clone github.com/ethanjli/pallet-example-minimal@main
```

Then you can apply the cloned pallet on your computer using the following sequence of `forklift`
CLI commands:
```
sudo -E forklift plt apply
```

Warning: this will replace all Docker containers on your Docker host with the package deployments
specified by this pallet and delete any Docker containers not specified by this pallet's package
deployments.

If your user is in the `docker` group (so that you don't need to use `sudo` when running `docker`
commands), then you can just run a single command instead of the two the commands listed above:

```
forklift plt switch github.com/ethanjli/pallet-example-minimal@main
```

### Validation

This pallet will bring up a web server at port 3000. If you open <http://localhost:3000> in your web
browser after deploying the pallet, you should see an NGINX page which prints some basic information
such as the current date. If you open <http://localhost:3000/whoami>, you should see another page
with some additional information (e.g. your browser's user agent).

## Licensing

Forklift packages deployed by this pallet have their own software licenses, as specified in the
definitions of those packages. Any source code provided with this Forklift pallet is covered by the
following information, except where otherwise indicated:

Copyright Ethan Li and Forklift project contributors

SPDX-License-Identifier: Apache-2.0 OR BlueOak-1.0.0

You can use the source code provided here either under the
[Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0)
or under the [Blue Oak Model License 1.0.0](https://blueoakcouncil.org/license/1.0.0);
you get to decide. We are making the software available under the Apache license because it's
[OSI-approved](https://writing.kemitchell.com/2019/05/05/Rely-on-OSI.html),
but we like the Blue Oak Model License more because it's easier to read and understand.
