FROM daskdev/dask:2021.9.1

RUN apt update
RUN DEBIAN_FRONTEND=noninteractive apt install -y \
    curl \
    iputils-ping \
    sudo \
    tzdata \
    vim

RUN pip install prefect[templates,viz,azure,kubernetes,redis]
RUN pip install crowd-kit toloka-kit
