FROM ubuntu:20.04

ARG API_SERVER_ADDRESS="127.0.0.1"

RUN apt-get update && \
    apt-get install -y git python3-pip && \
    pip3 install --upgrade pip && \
    pip3 install Flask && \
    pip3 install requests && \
    git clone https://github.com/DmitryBizyaev/sphinx-speech-recognition-manual-frontend.git && \
    cd sphinx-speech-recognition-manual-frontend && \
    sed -i "s/localhost/$API_SERVER_ADDRESS/g" app.py

WORKDIR /sphinx-speech-recognition-manual-frontend

CMD [ "flask", "run", "--host=0.0.0.0", "--port=5555" ]

EXPOSE 5555