# download-hf

### Installing

* Make symlink dir and Build Docker with the following command
```
ln -s /foo/bar/xxxxx ./volume/Data
docker compose build -e HUGGINGFACE_TOKEN=xxxxxxxxx
```

## Usage

* Attach Docker
```
docker exec -it dl01 /bin/bash
```

* Execution download-hf
```
docker compose up
docker exec dl01 git clone https://huggingface.co/datasets/foo/bar
```
