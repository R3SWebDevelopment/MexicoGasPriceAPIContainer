FROM python:3.8.9
LABEL authors="Ricardo Tercero Solis"

RUN apt-get -y update
RUN apt-get -y install git
RUN mkdir /app
RUN git clone -b '1.0.1' --single-branch --depth 1 https://github.com/R3SWebDevelopment/MexicoGasPriceAPI.git /app

WORKDIR /app

RUN pip install -r requirements.txt

ENTRYPOINT ["python", "-m", "flask", "run", "--host=0.0.0.0"]
