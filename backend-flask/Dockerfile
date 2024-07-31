
#take configuration from another container
FROM python:3.10-slim-buster

#Inside the container ser WORKDIR as below folder/create new folder
WORKDIR /backend-flask

#move from outside machine to docker 
COPY requirements.txt requirements.txt

# run inside container
RUN pip3 install -r requirements.txt

# copy everything from outside container to inside container
COPY . .

ENV FLASK_ENV=development


EXPOSE ${PORT}

#Command
#python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]