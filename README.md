# compose-postgres

Example Docker Compose PostgreSQL setup with database pre-seeding

- [https://docs.docker.com/guides/pre-seeding/](https://docs.docker.com/guides/pre-seeding/)
- [https://www.perplexity.ai/search/yaml-syntax-docker-dockerfile-ZDe.1wUETLmYgX2AW5tl5g](https://www.perplexity.ai/search/yaml-syntax-docker-dockerfile-ZDe.1wUETLmYgX2AW5tl5g)

```bash
docker compose \
    exec postgres \
    psql \
    -U ${POSTGRES_USER} \
    -d ${POSTGRES_DB} \
    -c "\COPY my_table FROM '/data/large_dataset.csv' CSV HEADER;"
```

```bash
sudo chown -R 5050:5050 ./backups
sudo chmod -R 755 ./backups
```

```bash
docker cp ./backups/ig.sql pgadmin:/var/lib/pgadmin/storage/your_email.com/
```
