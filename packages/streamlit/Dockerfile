FROM python:3.10-slim-buster
WORKDIR /app
COPY  . /app
RUN pip install --no-cache-dir -r requirements.txt
CMD ["streamlit", "run", "app.py"]
EXPOSE 8501
#$ docker run -p 8501:8501 template-image:0.1