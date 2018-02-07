# base image
FROM alpine:3.5

# install pip and python requirements
RUN apk add --update py2-pip

# copy files and install requirements
COPY app.py /usr/src/app/
COPY templates/index.html /usr/src/app/templates/
COPY requirements.txt /usr/src/app/
RUN pip install --no-cache-dir -r /usr/src/app/requirements.txt

# port
EXPOSE 5000

# run app when container will be started
CMD ["python", "/usr/src/app/app.py"]
