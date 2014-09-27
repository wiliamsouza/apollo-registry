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

Create to volumes folder one to be used locally and one to be syncronized with
the cluster for future use.

```
mkdir -p ~/.containers/apollo/registry/volumes/data
mkdir -p ~/.containers/local/registry/volumes/data
```

[fig](http://orchardup.github.io/fig/) is used to facilitate start and stop
of the docker containers.

```
cd apollo-registry
fig up -d
```

Common address
--------------

As root set more one ip address to `eth0`.

```
ifconfig eth0:0 172.16.16.16
```

Pushing images
--------------

Before push an image you need to build one, see `apollo/README.md`
or `apollo-nginx/README.md` for instruction how to build a `local`
image and push an image to a registry.
