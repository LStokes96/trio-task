From python:latest

# Install apt dependencies
RUN apt-get update -y
RUN apt-get install python3-venv python3-pip -y 

# Copy contents into image
COPY . .
 
# run pip dependencies
RUN python3 -m venv venv
RUN . venv/bin/activate
RUN pip3 install flask
RUN pip3 install flask-sqlalchemy
RUN pip3 install PyMySQL[rsa]

 

# Expose correct port
EXPOSE 5000


# Create an entrypoint
ENTRYPOINT ["python3", "app.py"]
