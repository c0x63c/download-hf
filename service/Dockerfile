FROM python:3.11

ARG HUGGINGFACE_TOKEN
ENV PYTHONUNBUFFERED=1 

# system
# python3
RUN apt update -y -q && DEBIAN_FRONTEND=noninteractive apt install -y -q --no-install-recommends \
    software-properties-common apt-utils \
    curl git git-lfs vim \
    && rm -rf /var/lib/apt/lists/*

# cd workdir and huggingface client install
WORKDIR /volume
RUN pip install -U "huggingface_hub[cli]" && git lfs install \
    && huggingface-cli login --token ${HUGGINGFACE_TOKEN} --add-to-git-credential

# shell
CMD ["/bin/bash"]
