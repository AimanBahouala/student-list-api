FROM python:2.7-stretch
COPY student*.py ./
RUN apt-get update -y && apt-get install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv
RUN mkdir data
COPY student*.json ./data
EXPOSE 5000
VOLUME ./data
CMD [ "python", "./student_age.py" ]
