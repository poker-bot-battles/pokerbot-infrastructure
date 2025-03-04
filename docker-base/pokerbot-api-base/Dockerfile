FROM openjdk:23-slim
COPY --from=python:3.11 / /
WORKDIR /app

RUN apt-get update && apt-get install -y cmake
RUN apt-get install -y clang
RUN pip install cython
RUN pip install eval7 open-spiel --no-cache-dir
RUN pip install poker-game-runner --no-deps
RUN pip install uvicorn fastapi python-multipart
