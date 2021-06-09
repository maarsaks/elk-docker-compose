1. Clone the repo.
2. Go to `elk-docker-compose` directory and create an empty directory named `data`.
3. Run `sudo chmod 600 ./filebeat/filebeat.yml && sudo chown root ./filebeat/filebeat.yml`.
4. Run `docker-compose up -d`.
5. Wait few minutes, open in browser http://localhost:5601 and use login `elastic` and password `password`.
6. From the left panel go to `Stack Management` under `Management`.
7. Under `Kibana` open `Index Patterns` and `Create index pattern`.
8. In `Index pattern name` field, enter `index-haproxy-*`, go `next`, in `Time field` choose `@timestamp` and `Create index pattern`.
9. From the left panel under `Analytics` open `Discover`,
 - choose `index-haproxy*` index pattern,
 - select `message` and `error.message` fields.