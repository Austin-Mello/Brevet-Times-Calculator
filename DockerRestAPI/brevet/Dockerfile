FROM python:3-onbuild
MAINTAINER Austin Mello "amello3@uoregon.edu"
RUN apt-get update -y
RUN apt-get install -y python-pip python-dev build-essential
# Copying source in current directory into the image
# python:3-onbuild expects the source in /usr/src/app
COPY . /usr/src/app
WORKDIR /usr/src/app
COPY requirements.txt .
RUN pip install -r requirements.txt
# Commands in a list
CMD ["python", "api.py"]
