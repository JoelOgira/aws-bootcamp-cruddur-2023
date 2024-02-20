FROM python:3.10-slim-buster

# Inside the container
# make a new directory called backend-flask inside the container
WORKDIR /backend-flask

# Copy from Outside container -> Into Inside container
# Contains all python libraries and depandancies needed to run the app
COPY requirements.txt requirements.txt

# Inside the container
# Install the python libraries used for the app
RUN pip3 install -r requirements.txt

# Copy from Outside container -> Into Inside container
# . means everything in current directory
# first period - /backend-flask (outside container)
# second period - /backend-flask (inside container)
COPY . .

# Set Environment Variables 
ENV FLASK_ENV=development

EXPOSE ${PORT}

# python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m", "flask", "run", "--host=0.0.0.0", "--port=4567" ]