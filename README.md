The main documentation for how to run the project is located in the fork, by pressing the fork you are transported to the main repository with more detailed documentation. However a simplified quick-start guide is put below 


## Prerequesites 

- Docker compose and docker is installed on the computer (https://docs.docker.com/compose/install/) (https://docs.docker.com/engine/install/).
- Git for cloning project (https://git-scm.com/install/)
- Optional but recommended is to have docker desktop installed (https://www.docker.com/products/docker-desktop/). 

## quick-start guide.

Any terminal can be used to access the project folder using, example is cloned to desktop
```
cd C:\Users\yourName\Desktop\ais-viz-backend\ntnu-data-bachelor-26-fork
```
The folder is now specifically the one that will be called ntnu-data-bachelor-26-fork to access.

when inside the folder docker commands can be run in terminal, also the amount of points that are gonna be generated can be changed in the "docker-compose" yaml source file. by going to the line command: ```["/db-migration", "-geojson-seed", "-reseed", "-anomaly-limit", "${ANOMALY_LIMIT:-100000}"]``` and changing the Anomaly Limit number, in the example it being 100000. this changes the amount of anomaly groups generated.


To build the docker project while inside of ntnu-data-bachelor-26-fork. write in the terminal ```docker compose up --build``` detach by pressing d when it is done.

The quickest way to get data generates is through the command ```docker compose --profile geojson-seed up --build```, also detach here when its done. 

After this is done then the database is seeded with the amount of data in ANOMALY_LMIT, and the frontend can be run. 
