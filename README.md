# build-ueransim

This repo contains the generation of the [UERANSIM](https://github.com/aligungr/UERANSIM) image, hosting an open-source SoA 5G UE and RAN (gNodeB) implementation. It can be considered as a 5G mobile phone and a 5G base station. 

## WorkFlow

The image is built inside vagrant Fedora VM using buildah. Once the image is built it is pushed to a registry. The image pushed in a registry will be consumed by k8s.

## Quickstart


1. Deploy and log in vagrant VM:

   ```
   vagrant up
   vagrant ssh
   cd /vagrant
   ```

2. Build the ueransim image:

   ```
   build-ueransim
   ```

3. Push ueransim container to registry (in this case an insecure registry):

   ```
   load-ueransim
   ```

4. Deploy on your preferred container cluster platform. See this [repo](https://github.com/jnunyez/kindk8s-ueransim) for deploying UERANSIM in k8s.

## ToDo

- Generalize entrypoint of generated image to include UERANSIM `nr-cli` exposing a CLI to manage 5G UE and 5G gNodeB. 
- Permit UE deployments at scale in the current entrypoint