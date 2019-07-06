# Download and install a very lightweight linux distro.
FROM alpine:3.7

# A Little info
LABEL Description="Dockerized my dummy-api as an example of how to create an image"

# Copies the dummy-api files.
COPY ./dummy-api/ /dummy-api/

# Installs Python3
RUN apk --update --no-cache add python3 python3-dev py3-pip

# Updates PIP just so we don't get those pesky warning messages...
#RUN pip3 install --upgrade pip

# Installs required stuffs...
RUN pip3 install -r /dummy-api/requirements.txt

# Defining working directory
WORKDIR /dummy-api/

# Starts the API
CMD ["python3", "app.py"]