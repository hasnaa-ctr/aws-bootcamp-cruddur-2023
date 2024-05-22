FROM python:3.10-slim-buster
# make a new folder inside container
WORKDIR /backend-flask
# outside Container -> inside Container
COPY requirements.txt requirements.txt
# instll the python lib used for the app
RUN pip3 install -r requirements.txt
# Outside Container - > Inside Container
# . means everything in the current directory
# first period ./ backend-flask (outside container)
# second period ./ backend-flask (inside container)
COPY . .
## Set Enviroment Variables (Env Vars)
# Inside Container and wil remain set when the container is runing
ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]
# python3 -m flask run --host=0.0.0.0 --port=4567