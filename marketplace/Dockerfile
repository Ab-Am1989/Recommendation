FROM python

ENV FLASK_APP=marketplace.py
ENV RECOMMENDATIONS_HOST=localhost
EXPOSE 5000

RUN mkdir /service

COPY protobufs/ /service/protobufs/
COPY marketplace/ /service/marketplace/
WORKDIR /service/marketplace
RUN python -m pip install --upgrade pip
RUN python -m pip install -r requirements.txt

ENTRYPOINT [ "flask", "run", "--host=0.0.0.0" ]