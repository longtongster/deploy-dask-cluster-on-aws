FROM python:3.10.12-slim

# create app directory and move in the directory
WORKDIR app

# copy the requirements.txt in the app directory in the container
COPY ./requirements.txt .

# install and upgrade pip
RUN pip3 install --upgrade pip

# install the dependencies in the requirement.txt
RUN pip3 install -r requirements.txt

# expose all these port
EXPOSE 8786 8787 30000-65535

# execute `dask scheduler --host 0.0.0.0` in container when 
# we run the container
CMD ["dask", "scheduler", "--host", "0.0.0.0"]
#CMD ["dask", "scheduler"]
