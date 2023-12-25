FROM nvidia/cuda:12.2.0-runtime-ubuntu20.04 as base

RUN apt-get update -y && apt-get install -y python3.9 python3.9-distutils curl
RUN curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
RUN python3.9 get-pip.py

FROM base
WORKDIR /app
COPY . /app
RUN pip3 install .[model_worker,webui] pydantic==1.10.13