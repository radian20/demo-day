# Demo

Setting the right Airflow user
On Linux, the quick-start needs to know your host user id and needs to have group id set to 0. Otherwise the files created in dags, logs and plugins will be created with root user ownership. You have to make sure to configure them for the docker-compose:
```
mkdir -p ./dags ./logs ./plugins ./config
```
Initialize the database
On all operating systems, you need to run database migrations and create the first user account. To do this, run.
```
docker compose up airflow-init
```
After initialization is complete, you should see a message like this:
``` bash
airflow-init_1       | Upgrades done
airflow-init_1       | Admin user airflow created
airflow-init_1       | 2.6.1
start_airflow-init_1 exited with code 0
```
The account created has the login airflow and the password airflow.

After all we can run 
```
docker compose down && docker compose up -d
```

To see jupyter logs
```
docker logs -f course_jupyterlab
```
<b>Airflow</b> available localhost:8080

<b>PgAdmin</b> available localhost:5050



