FROM python:3.8-slim-buster

WORKDIR /app/frontend
COPY . .


RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    ca-certificates \
    cmake \
    build-essential \
    gcc \
    g++


RUN pip install --upgrade pip && \
    pip install --ignore-installed -r requirements.txt

EXPOSE 8501

ENTRYPOINT ["streamlit", "run"]
CMD ["main.py"]