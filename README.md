# build-oai-gnb

This repo contains the generation of the oaips. 

## WorkFlow

The image is built inside vagrant Fedora VM using `buildah`. The Vagrant VM is used to build necessary libraries for Universal Hardware Driver (UHD) and OAI gNB in SA mode libraries.  Once the libraries are built they are moved to RH Universal Base Image (UBI) image using `buildah`.  The resulting image is pushed into a registry that will be consumed by k8s.

## Quickstart


1. Deploy and log in vagrant VM:

   ```
   vagrant up
   vagrant ssh
   cd work
   ```

2. Build the image:
   
   ```
   ./build-gnb
   ```
   

3. Push image labelled as `oai_gnb` container to registry (in this case an insecure registry).

   ```
   load-image oai_gnb
   ```

