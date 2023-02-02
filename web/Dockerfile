FROM python:3.10.6-slim

COPY . /app
WORKDIR /app 

RUN python -m env /opt/env

RUN /opt/env/bin/pip install -r requirements.txt && \
chmod +x entrypoint.sh

# entrypoint.sh is actuall for the script to enter the virtualenv 
# hence we dont need to explicitly activate the virtual env in the dockerfile
CMD ["/app/entrypoint.sh"]  