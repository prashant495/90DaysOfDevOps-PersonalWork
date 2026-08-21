**What are Docker Layers?**

A Docker layer is a read-only filesystem change that becomes part of a Docker image.

Docker builds an image layer by layer, usually based on the instructions in the Dockerfile.

FROM ubuntu
RUN apt-get update
RUN apt-get install -y nginx
COPY index.html /var/www/html/
CMD ["nginx", "-g", "daemon off;"]

             Docker Image
          ┌───────────────┐
          │ CMD           │ ← Layer
          ├───────────────┤
          │ COPY          │ ← Layer
          ├───────────────┤
          │ RUN install   │ ← Layer
          ├───────────────┤
          │ RUN update    │ ← Layer
          ├───────────────┤
          │ Ubuntu        │ ← Base layer
          └───────────────┘

      Layers can be shared between images.

      Image A                 Image B

Ubuntu                  Ubuntu
   ↓                       ↓
Python                  Nginx

Both images can reuse the same underlying Ubuntu layers instead of storing duplicate copies.

This saves disk space.

When pushing an image to a registry, Docker can reuse layers that already exist.
This saves:

Time
Bandwidth
Storage
