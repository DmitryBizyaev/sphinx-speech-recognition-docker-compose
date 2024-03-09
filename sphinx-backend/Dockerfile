FROM ubuntu:20.04

RUN apt-get update && \
    apt-get install -y git python3-pip && \
    pip3 install --upgrade pip && \
    pip3 install pocketsphinx && \
    git clone https://github.com/DmitryBizyaev/sphinx-speech-recognition-manual.git && \
    cd sphinx-speech-recognition-manual

WORKDIR /sphinx-speech-recognition-manual

CMD [ "python3", "request_handler.py" ]

EXPOSE 5000