# Postgres pg_dump

To configure dump over pg_dump when using docker follow these steps:


1. Open posgresql configuration (usually it is located in `/etc/postgresql/<your_postgres_version>/main/postgresql.conf` ) and add 

   ```sql
   listen_addresses = '172.27.0.1'
   ```
2. In the file: `/etc/postgresql/<your_postgres_version>/main/pg_hba.conf` add a new entry:  `host all all 172.27.0.0/16 md5`
3. Restart PostgreSQL


:::info
There 172.27.0.0/16 could be replaced by your custom network

:::