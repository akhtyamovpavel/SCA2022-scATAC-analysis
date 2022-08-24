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
jupyter notebook --ip 0.0.0.0 --port 8888 --no-browser --allow-root
```

Outside container go to site http://locahost:9021 and run Jupyter notebook in your browser.

## Links

* [Presentation](https://docs.google.com/presentation/d/1n7tDgpacqBI9YFgHfQJZx52yk23EisFH5CDOLjhGEeA/edit?usp=sharing)
* [Datasets](Datasets)

