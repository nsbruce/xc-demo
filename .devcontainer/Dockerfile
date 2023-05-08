FROM python:3.11

ENV container docker \
    PYTHONBUFFERED=1

RUN curl -sSL https://install.python-poetry.org | POETRY_VERSION=1.3.0 python3.11 -

ENV PATH "$PATH:/root/.local/bin"

RUN poetry config virtualenvs.create false

RUN curl -L -o /usr/local/bin/xc https://github.com/joerdav/xc/releases/download/v0.4.1/xc_0.4.1_linux_386 \
    && chmod +x /usr/local/bin/xc \
    && xc --complete