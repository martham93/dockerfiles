FROM windj007/jupyter-keras-tools

MAINTAINER Max Joseph <maxwell.b.joseph@colorado.edu>

RUN apt-get update -qq \
 && apt-get install --no-install-recommends -y \
    git

ENV USE_SETUPCFG=0

# install dependencies from python packages
RUN pip --no-cache-dir install \
    awscli \
    netCDF4

EXPOSE 8888

WORKDIR "/notebook/"

ENTRYPOINT ["/entrypoint.sh"]
CMD [ "jupyter", "notebook", "--ip=0.0.0.0", "--allow-root" ]

