Apollo registry
===============

It is [docker-registry](https://github.com/dotcloud/docker-registry)
used for hosting/delivering repositories and images for containers.

It can be stared in your local development box using local storage during
development and inside your cluster using s3 for storage on production.

Getting code
------------

```
git clone https://github.com/wiliamsouza/apollo-registry.git
```

Running locally
---------------

```
mkdir -p ~/.containers/apollo/registry/volumes/data
```

```
cd apollo-registry
fig up -d
```

[fig](http://orchardup.github.io/fig/) is used to facilitate start and stop
of the docker containers.

Pushing images
--------------

Before push an image you need to build one, see `apollo/README.md`
or `coreos-nginx/README.md` for instruction how to build a `development`
image and push an image to a registry.
