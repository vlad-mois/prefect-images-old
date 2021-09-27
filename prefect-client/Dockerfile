FROM vladmois/toloka-dask

ENV LC_ALL=C.UTF-8
ENV LANG=C.UTF-8
RUN pip install prefect

ARG APOLLO_URL=localhost
ARG PREFECT_UI_URL=localhost
ARG PREFECT__ENGINE__EXECUTOR__DEFAULT_CLASS=prefect.executors.DaskExecutor
ARG PREFECT__ENGINE__EXECUTOR__DASK__ADDRESS=tcp://localhost:8786

COPY config.toml /root/.prefect/
RUN prefect backend server

CMD bash
