# to build for local architecture: 			docker image build -t flask_basic_app .
# to run locally:							docker run -p 5066:80 -d flask_basic_app
# check app locally:						curl 0.0.0.0:5066

FROM python:3.8-alpine

# copy the requirements file into the image
COPY ./requirements.txt /app/requirements.txt

# switch working directory
WORKDIR /app

# install the dependencies and packages in the requirements file
RUN pip install -r requirements.txt

# copy every content from the local file to the image
COPY ./app.py /app/app.py

# configure the container to run in an executed manner
ENTRYPOINT [ "python" ]
CMD ["app.py" ]
