
# usage

```
➜ docker-compose up -d
Creating airflow-docker-compose-example_db_1            ... done
Creating airflow-docker-compose-example_airflow_redis_1 ... done
Creating airflow-docker-compose-example_airflow_scheduler_1 ... done
Creating airflow-docker-compose-example_airflow_webserver_1 ... done
Creating airflow-docker-compose-example_airflow_worker_1    ... done
Creating airflow-docker-compose-example_airflow_flower_1    ... done


➜ docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED              STATUS              PORTS                                        NAMES
5ab02a419db1        airflow:latest      "./wait-for-it.sh ai…"   3 seconds ago        Up 1 second         5555/tcp, 8793/tcp, 0.0.0.0:8080->8080/tcp   airflow-docker-compose-example_airflow_webserver_1
91859cca3601        airflow:latest      "./wait-for-it.sh ai…"   3 seconds ago        Up 1 second         8080/tcp, 0.0.0.0:5555->5555/tcp, 8793/tcp   airflow-docker-compose-example_airflow_flower_1
407a7cc95f4e        airflow:latest      "./wait-for-it.sh ai…"   3 seconds ago        Up 2 seconds        5555/tcp, 8080/tcp, 8793/tcp                 airflow-docker-compose-example_airflow_worker_1
0a97093d4666        airflow:latest      "./wait-for-it.sh db…"   4 seconds ago        Up 3 seconds        5555/tcp, 8080/tcp, 8793/tcp                 airflow-docker-compose-example_airflow_scheduler_1
ac0d4cde9429        mysql:5.7           "docker-entrypoint.s…"   5 seconds ago        Up 3 seconds        0.0.0.0:3306->3306/tcp, 33060/tcp            airflow-docker-compose-example_db_1
ff3c191d16be        redis:3.2           "docker-entrypoint.s…"   5 seconds ago        Up 4 seconds        6379/tcp                                     airflow-docker-compose-example_airflow_redis_1
```

# ui

![](airflow-ui.jpg)