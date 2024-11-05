FROM python:3.10.12-slim

WORKDIR app
COPY ./requirements.txt .

RUN pip3 install --upgrade pip

RUN pip3 install -r requirements.txt

EXPOSE 8786 8787 30000-65535

CMD ["dask", "scheduler", "--host", "0.0.0.0"]
#CMD ["dask", "scheduler"]
