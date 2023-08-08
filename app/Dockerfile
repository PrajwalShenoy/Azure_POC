FROM python:latest

ARG flaskEnv
WORKDIR /flaskApp
COPY ./requirements.txt /flaskApp
RUN pip install -r requirements.txt
COPY . /flaskApp/app
ENV flaskEnv=$flaskEnv
EXPOSE 80

CMD ["flask", "--app", "app", "run", "--host", "0.0.0.0", "-p", "80", "--debug"]