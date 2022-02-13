# aspera downloads container

To learn more about aspera downloads:

https://idr.openmicroscopy.org/about/download.html


The docker image, recommended by idr:

https://hub.docker.com/u/imagedata

## Usage

`docker run -ti --rm -v /tmp/data/idr0008:/data imagedata/download idr0008 . /data`

### Partial downloads

`$ ascp -TQ -l40m -P 33001 -i "path/to/asperaweb_id_dsa.openssh" idr0040@fasp.ebi.ac.uk:20180215/3105/Pos0 /tmp/data/idr0040_partial`