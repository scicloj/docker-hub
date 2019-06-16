## libpython-clj

Image opens up a repl port on 8888 you can connect to in order to test out
python bindings.

```console
$ docker build . -f Dockerfile.libpythonclj -t libpythonclj-docker
...

$ docker run libpythonclj-docker
```
