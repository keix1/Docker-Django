
# golang:onbuild automatically copies the package source, 
# fetches the application dependencies, builds the program, 
# and configures it to run on startup 
FROM python:3
LABEL Name=docker-django Version=0.0.1 
EXPOSE 3000
WORKDIR /web
ENV PYTHONUNBUFFERED 1

COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

CMD [ "python", "/web/manage.py", "runserver"]

# For more control, you can copy and build manually
# FROM golang:latest 
# LABEL Name=docker-django Version=0.0.1 
# RUN mkdir /app 
# ADD . /app/ 
# WORKDIR /app 
# RUN go build -o main .
# EXPOSE 3000 
# CMD ["/app/main"]
