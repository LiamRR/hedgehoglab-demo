FROM python:3.13-alpine

# Install pip
RUN python -m pip install --upgrade pip

WORKDIR /app

# Install python dependencies
COPY requirements.txt ./

RUN python -m pip install -r requirements.txt

COPY . .

EXPOSE 8000

CMD ["uvicorn", "main:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]
