
# Build and run
docker-compose up --build -d

# To get token from running container:
docker exec -it jupdoc-jupyter-1 /opt/venv/bin/jupyter notebook list


# To access bash container from Git Bash
winpty docker exec -it jupdoc-jupyter-1 //bin//bash

