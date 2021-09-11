FROM tiangolo/uvicorn-gunicorn-fastapi:python3.7

COPY ./app /app
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -y
RUN apt install libgl1-mesa-glx -y
RUN apt-get install 'ffmpeg'\
    'libsm6'\
    'libxext6'  -y
RUN pip3 install --upgrade pip
RUN pip3 install opencv-python==4.3.0.38
COPY requirements.txt .
RUN pip3 --no-cache-dir install -r requirements.txt

