FROM python:3.9-slim-buster
RUN  pip3 --version;
# SHELL ["/bin/bash", "-c"]
# RUN /bin/bash -c "echo 'hello world' > hello.html;"
# RUN [ "/bin/bash", "-c", "echo 'hello world' >> y.html;" ]

RUN mkdir myapp
COPY DevOps-Challenge-Demo-Code ./myapp
WORKDIR /myapp
RUN pip3 install -r requirements.txt

# port 8000 is the application port
EXPOSE 8000
# Port 6379 is redis port 
EXPOSE 6379 

ENTRYPOINT ["/bin/bash" , "-c", "export $(cat .env | xargs) && python hello.py"]
