# Buildah

This repository provides a unofficial docker image to use buildah in a container.

--

The Buildah package provides a command line tool that can be used to:

* create a working container, either from scratch or using an image as a starting point
* create an image, either from a working container or via the instructions in a Dockerfile
* images can be built in either the OCI image format or the traditional upstream docker image format
* mount a working container's root filesystem for manipulation
* unmount a working container's root filesystem
* use the updated contents of a container's root filesystem as a filesystem layer to create a new image
* delete a working container or an image
* rename a local container

## Execution

Buildah requires container-mounts at:

- /var/run/containers/storage
- /var/lib/containers/storage

Additionaly the it requires the capability `--cap-add=SYS_ADMIN` or needs to be executed as privilegied.
