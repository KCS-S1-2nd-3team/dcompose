FROM python:3.10.7-alpine3.16
COPY ./sourcecode /sourcecode
WORKDIR /sourcecode
RUN pip install -r ./requirements.txt
EXPOSE 35001
CMD ["python", "app.py"]
