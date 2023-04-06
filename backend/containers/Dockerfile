from python:3.11

#container working directory
WORKDIR /app

#copy requirements
copy ./requirements.txt .
run pip install -r requirements.txt

#copying src and logs
copy ./lightning_logs/ ./lightning_logs
copy ./src/ ./src

expose 3000
ENV FLASK_APP=app.py
cmd ["python", "-m", "flask", "run" , "--host=0.0.0.0", "--port=3000"]