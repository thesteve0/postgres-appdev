# postgres-appdev (deprecated)
This container image was created when I worked at Crunchy Data. It was originally called crunchy-postgres-appdev. They have since removed the repo from GitHub and the image from Docker Hub. 
I still had an image on my machine. I renamed it to remove any reference to Crunchy to avoid anyone thinking this image was still affiliated with Crunchy Data in way

I retagged it to ghcr.io/thesteve0/postgres-appdev

There is no future development on this image. It is forever frozen in time at:
```PostgreSQL 12.3 on x86_64-pc-linux-gnu, compiled by gcc (GCC) 4.8.5 20150623 (Red Hat 4.8.5-39), 64-bit```

As long as you don't need any features or security fixes that occured after that release you should be fine. 
Obviously this means I don't think this image should ever be run in production. 

It has all the spatial extension and embedded R. It is based off of the https://github.com/CrunchyData/crunchy-containers postgres-gis container.

The goal of this project was to produce a container that makes it easy and simple for application developers to get started with PostgreSQL using containers.This is a non-supported, not intended for production release. 

You can set the following environment variables with the `docker run -e` command:

| Variable name | default |
| --- | --- |
| PG_USER= | rnduser2w3 |
| PG_PASSWORD= |  * required that you provide this |
| PG_DATABASE= | mydb |
| PG_ROOT_PASSWORD= | set to the same password as PG_USER |
| PG_PRIMARY_PORT= | 5432 |
