# build-oai-gnb

This repo contains the generation of the oaips. 

## WorkFlow

The image is built inside vagrant Fedora VM using buildah. Once the two images are built they are pushed to a registry in RH ubi image. The image pushed in a registry will be consumed by k8s.

## Quickstart


1. Deploy and log in vagrant VM:

   ```
   vagrant up
   vagrant ssh
   cd /vagrant
   ```

2. Build the image:
	* Building open5gs base image:
   
   ```
   build-gnb
   ```
   

3. Push image (webui or open5gs) container to registry (in this case an insecure registry).

   * Push open5gs base image:
   ```
   load-image oai_gnb
   ```

