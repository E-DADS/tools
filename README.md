# E-DADS Resources
Various tools and resources for the E-DADS project

1. [FreeSurfer 7.1.1 BIDS App](#freesurfer-711-bids-app-container)
2. [MRI-QC 0.16.1 BIDS App](#mriqc-0161-bids-app-container)

<hr/>

## FreeSurfer 7.1.1 BIDS-App container
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

## MRIQC 0.16.1 BIDS-App container
- To use this version, the easiest way to build a singularity container is via Poldrack Lab's dockerhub:
```
docker pull poldracklab/mriqc:0.16.1
```

<hr/>
