# This is a simple Dockerfile to use while performing exploration (for deployment consider smaller images)
#FROM --platform=linux/amd64 python:3.9.6
#FROM quay.io/jupyter/minimal-notebook
FROM --platform=linux/amd64 quay.io/jupyter/scipy-notebook

USER root

RUN apt-get update
RUN apt-get install libmagic1 -y

# Best Libraries for Geo Visualisation, Good overview:
# https://towardsdatascience.com/best-libraries-for-geospatial-data-visualisation-in-python-d23834173b35

# Install main packages using Pip - This is used when Conda does not work!
COPY requirements.txt ./requirements.txt
RUN pip install -r requirements.txt

#WORKDIR notebooks

EXPOSE 8888
EXPOSE 9000
