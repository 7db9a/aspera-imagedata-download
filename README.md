# aspera downloads container

To learn more about aspera downloads:

https://idr.openmicroscopy.org/about/download.html


The docker image, recommended by idr:

https://hub.docker.com/u/imagedata

https://github.com/IDR/aspera-client-docker

## Work pattern

Find the study

https://github.com/IDR/idr-metadata

Go to `screenA`

https://github.com/IDR/idr-metadata/tree/master/idr0010-doil-dnadamage/screenA

Open tsv file

https://github.com/IDR/idr-metadata/blob/master/idr0010-doil-dnadamage/screenA/idr0010-screenA-plates.tsv

You'll need the equivalent

docker run -ti --rm -v /tmp/data:/data imagedata/download idr0001 `20151116-verified`/JL_120731_S6A /data/JL_120731_S6A

See her for an example:

https://github.com/IDR/idr-metadata/blob/master/idr0001-graml-sysgro/screenA/idr0001-screenA-plates.tsv

/uod/idr/filesets/idr0001-graml-sysgro/`20151116-verified`/JL_120731_S6A

## Usage

`docker run -ti --rm -v /tmp/data/idr0008:/data imagedata/download idr0008 . /data`

`docker run -ti --rm -v /tmp/data:/data imagedata/download idr0001 20151116-verified/JL_120731_S6A /data/JL_120731_S6A`

`docker run -ti --rm -v /tmp/data:/data imagedata/download idr0010 1-23 /data/1-23`


### Partial downloads

`$ ascp -TQ -l40m -P 33001 -i "path/to/asperaweb_id_dsa.openssh" idr0040@fasp.ebi.ac.uk:20180215/3105/Pos0 /tmp/data/idr0040_partial`