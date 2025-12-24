FROM python:latest

# create venv
RUN python -m venv /opt/venv/
ENV PATH=/opt/venv/bin:$PATH


WORKDIR /app

# copy local file to contanier destination
COPY requirements.txt /tmp/requirements.txt
# run within container while building
RUN pip install -r /tmp/requirements.txt

COPY ./src /app

CMD ["python", "-m", "http.server", "8000"]