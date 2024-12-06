FROM python:3.9

# Install curl and other dependencies
RUN apt-get update && apt-get install -y curl bash

# Install Poetry using the official installation script
RUN curl -sSL https://install.python-poetry.org | python3 -

# Add Poetry to PATH
ENV PATH="/root/.local/bin:$PATH"

WORKDIR /app

COPY . .

RUN poetry install

EXPOSE 8000

CMD ["sh", "-c", "poetry run bash ./prestart.sh && poetry run uvicorn app.main:app --reload"]


