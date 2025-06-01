FROM python:3.11-slim
WORKDIR /app
COPY . /app
RUN pip install "fastapi[standard]"
CMD ["fastapi", "run", "demo.py"]