# SCA2022-scATAC-analysis

Notebooks are located in the [notebooks](notebooks) folder.

There are two notebooks:
* [Clustering.ipynb](notebooks/Clustering.ipynb)
* [StreamTutorial.ipynb](notebooks/StreamTutorial.ipynb) - notebooks of STREAM tool to build scATAC pseudo-time

## Prerequisites

#### Pull Docker image
```
docker pull akhtyamovpavel/stream-atacseq
```

#### Clone repo
```
https://github.com/akhtyamovpavel/SCA2022-scATAC-analysis.git
cd SCA2022-scATAC-analysis
```

#### Run Docker container

This is example how to run Docker container

```
docker run -d --name streamatac --entrypoint /bin/bash -v $PWD:/data -w /data -p 9021:8888 akhtyamovpavel/stream-atacseq
```

Exec into container:
```
docker exec -it streamatac bash
cd /data
jupyter notebook --ip 0.0.0.0 --port 8888 --no-browser --allow-root
```

Outside container go to site http://locahost:9021 and run Jupyter notebook in your browser.

## Download datasets

1. Download datasets from Yandex.Disk
2. Put folder with contents to `datasets` folder

## Links

* [Presentation](https://docs.google.com/presentation/d/1n7tDgpacqBI9YFgHfQJZx52yk23EisFH5CDOLjhGEeA/edit?usp=sharing)
* [Datasets](https://disk.yandex.ru/d/K6VSWZOEg-81ig)

## References
* [STREAM](https://github.com/pinellolab/STREAM)
* [scopen](https://github.com/CostaLab/scopen)
* Buenrostro JD, Corces MR, Lareau CA, Wu B et al. Integrated Single-Cell Analysis Maps the Continuous Regulatory Landscape of Human Hematopoietic Differentiation. Cell 2018 May 31;173(6):1535-1548.e16.

