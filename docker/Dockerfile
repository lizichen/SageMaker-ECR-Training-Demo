FROM python:3.8.0

LABEL maintainer="lc3397"

ENV PYTHONPATH "${PYTHONPATH}:/project"

WORKDIR /

RUN pip install poetry
COPY pyproject.toml *.lock /
RUN poetry config virtualenvs.create false && poetry install --no-interaction --no-ansi

COPY code/* /

ENTRYPOINT ["python", "main.py"]