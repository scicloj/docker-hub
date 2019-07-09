FROM clojure:openjdk-11-tools-deps

EXPOSE 8888

RUN echo "deb http://fr.archive.ubuntu.com/ubuntu bionic main" >> /etc/apt/sources.list &&\
    apt-get update &&\ 
    apt-get install libpython3.6-dev python3-pip -y --allow-unauthenticated &&\
    pip3 install numpy &&\
    echo '{:deps {cnuernber/libpython-clj {:mvn/version "0.12"} nrepl/nrepl {:mvn/version "0.6.0"} org.clojure/tools.deps.alpha {:mvn/version "0.6.496"} cider/cider-nrepl {:mvn/version "0.21.1"}} :aliases {:nREPL {:extra-deps {nrepl/nrepl {:mvn/version "0.6.0"}}}}}' > deps.edn &&\
    echo '{:bind "0.0.0.0" :port 8888}' > .nrepl.edn &&\
    clj -Sforce < /dev/null >&0

CMD ["clj", "-R:nREPL", "-m", "nrepl.cmdline", "--middleware", "[cider.nrepl/cider-middleware]"]