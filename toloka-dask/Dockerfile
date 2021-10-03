FROM daskdev/dask:2021.9.1

RUN apt update
RUN DEBIAN_FRONTEND=noninteractive apt install -y \
    curl \
    iputils-ping \
    sudo \
    tzdata \
    vim

RUN pip install --no-cache-dir prefect[azure,kubernetes,redis,templates,viz]
RUN pip install --no-cache-dir crowd-kit toloka-kit ipython 
RUN pip install --no-cache-dir torch transformers
