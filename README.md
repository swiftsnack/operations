# operations


1. Install Docker on server

	https://docs.docker.com/install/linux/docker-ce/ubuntu/#set-up-the-repository


2. Run

`ssh -nNT -L $(pwd)/docker.sock:/var/run/docker.sock user@host`
`export DOCKER_HOST=unix://$(pwd)/docker.sock`
`rsync -r traefik.toml swiftsnack:traefik/traefik.toml`
`docker-compose up -d`