# E-DADS Resources
Various tools and resources for the E-DADS project

1. [FreeSurfer 7.1.1 BIDS App](#freesurfer-711-bids-app-docker-container)

<hr/>

## FreeSurfer 7.1.1 BIDS-App Docker container
- Source code (fork of [BIDS-App/freesurfer](https://github.com/BIDS-Apps/freesurfer)): [github.com/e-dads/freesurfer](https://github.com/e-dads/freesurfer)
- Get the pre-built container from [Neil's dockerhub](https://hub.docker.com/r/noxtoby/edads/tags): `docker pull noxtoby/edads:freesurfer7p1p1`
- Contact: [Neil](https://github.com/noxtoby) at UCL

Running this container on a cluster? Of course you are!<br/>
This is how to use docker and [docker2singularity](https://github.com/singularityhub/docker2singularity) to convert the container to a singularity image:
```
docker run \
-v /var/run/docker.sock:/var/run/docker.sock \
-v /path/to/output/folder:/output \
--privileged -t --rm \
singularityware/docker2singularity \
noxtoby/edads:freesurfer7p1p1
```

<hr/>
