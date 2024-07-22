FROM squidfunk/mkdocs-material:latest

ENV REQUIREMENT_DIR="/tmp"

COPY requirements.txt ${REQUIREMENT_DIR}/requirements.txt
RUN pip install --requirement ${REQUIREMENT_DIR}/requirements.txt && \
    rm ${REQUIREMENT_DIR}/requirements.txt