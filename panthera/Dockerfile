FROM simplect/clojupyter:0.2.2

EXPOSE 8888

# For building locally select your favorite mirror
ENV REPO "http://fr.archive.ubuntu.com/ubuntu bionic main"

RUN echo "deb http://fr.archive.ubuntu.com/ubuntu bionic main" >> /etc/apt/sources.list &&\
    apt-get update &&\
    apt-get install libpython3.6-dev python3-pip -y --allow-unauthenticated &&\
    pip3 install numpy pandas jinja2 xlrd

CMD ["jupyter", "notebook", "--log-level=ERROR", "--allow-root"]