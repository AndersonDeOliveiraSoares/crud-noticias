FROM python:3.8.0

WORKDIR /usr/app

COPY . .

RUN pip3 install -r requirements.txt

EXPOSE 8000

CMD [ "python3", "app.py" ]