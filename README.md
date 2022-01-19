# psql_com.md


PSQL



* sudo apt update
* sudo apt install postgresql postgresql-contrib

sudo -i -u postgres
psql
sudo -u postgres psql

createuser --interactive



CREATE DATABASE guru99;
create user myuser with encrypted password 'mypass';
grant all privileges on database mydb to myuser;

ALTER USER myuser WITH SUPERUSER;


GRANT CONNECT ON DATABASE database_name TO username;

GRANT USAGE ON SCHEMA database_name TO username;

GRANT SELECT, INSERT, UPDATE, DELETE ON ALL TABLES IN SCHEMA database_name TO username;

GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA schema_name TO username;

GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA schema_name TO username;

GRANT ALL PRIVILEGES ON DATABASE database_name TO username;

ALTER USER username CREATEDB;



ALTER USER username WITH NOSUPERUSER;

ALTER DATABASE db RENAME TO newdb;

Those statements above only affect the current existing tables. To apply to newly created tables, you need to use alter default.

ALTER DEFAULT PRIVILEGES
FOR USER username
IN SCHEMA schema_name
GRANT SELECT, INSERT, UPDATE, DELETE ON TABLES TO username;

REVOKE CONNECT ON DATABASE dc FROM public;

CREATE EXTENSION IF NOT EXISTS citext WITH SCHEMA public;


