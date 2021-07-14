# build-ueransim

this repo builds 5G-NR artifacts for subsequent deployments.

## Rationale

This repo contains the generation of [ueransim](https://github.com/aligungr/UERANSIM).

## Quickstart


1. Deploy and log in fedora VM

   ```
   vagrant up
   vagrant ssh
   cd /vagrant
   ```

2. build ueransim

   ```
   build-ueransim
   ```
3. push ueransim container to registry

   ```
   load
   ```