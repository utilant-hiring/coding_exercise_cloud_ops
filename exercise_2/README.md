# Containerizing Web App

## Background:
A data scientist has created a new python web app (code in `my_app` directory) that now needs to be containerized before being deployed. The app has been tested using python 3.8, and requires the packages in `requirements.txt`. The app is launched via the command:
```
gunicorn my_app.main:app -w 4 -k uvicorn.workers.UvicornWorker --bind=0.0.0.0:8000
```

## Exercise:
Complete the `Dockerfile` in this directory to containerize the web app. Once completed, the following linux commands (run in this directory):
```
docker build -t hello-world .
docker run -dp 8000:8000 hello-world
curl localhost:8000
```
should return `{"message":"Hello World"}`.

Feel free to add comments to the `Dockerfile` as you see fit.