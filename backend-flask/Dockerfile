#####
# Create a Docker Image
#####

FROM python:3.10-slim-buster

# Inside Container
# Make a new folder inside container
WORKDIR /backend-flask

# Outside Container -> Inside Container
# Contains the libraries want to install to run the app
COPY requirements.txt requirements.txt

# Inside Container
# Install the Python libraries used for the app
RUN pip3 install -r requirements.txt

# Outside Container -> Inside Container
# . means everything in the current directory
COPY . .

# Set Environment Variables (Env Vars)
# Inside Container
ENV FLASK_ENV=development

EXPOSE ${PORT}

# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]