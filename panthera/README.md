## panthera

A ready-to-use image for [panthera](https://github.com/alanmarazzi/panthera) on Jupyter.

To run

```bash
docker run --rm -p 8888:8888 -v your/path:/home/jovyan/notebooks panthera
```

To use panthera you have to install it, to do it launch this in a cell:

```clojure
(require '[clojupyter.misc.helper :as helper])
(helper/add-dependencies '[panthera "REQUIRED-VERSION"])
:ok
```