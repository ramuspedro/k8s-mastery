FROM python:3.6.6-alpine
COPY sa /app
WORKDIR /app
RUN apk add gcc musl-dev libffi-dev openssl-dev python3-dev
RUN pip3 install -r requirements.txt && \
    python3 -m textblob.download_corpora
EXPOSE 5000
ENTRYPOINT ["python3"]
CMD ["sentiment_analysis.py"]
