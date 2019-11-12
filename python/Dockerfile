FROM python:latest
USER root

RUN apt-get update
RUN apt-get -y install locales && \
    localedef -f UTF-8 -i ja_JP ja_JP.UTF-8
ENV LANG ja_JP.UTF-8
ENV LANGUAGE ja_JP:ja
ENV LC_ALL ja_JP.UTF-8
ENV TZ JST-9
ENV TERM xterm-256color

RUN apt-get install -y vim less nodejs
RUN pip install --upgrade pip
RUN pip install --upgrade setuptools
RUN pip install pipenv jupyterlab
RUN jupyter serverextension enable --py jupyterlab

EXPOSE 8888

CMD ["jupyter", "lab", "--ip=0.0.0.0", "--allow-root"]