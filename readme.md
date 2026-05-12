# DB Playground

The repository has a simple docker-compose file and a few scripts to set up any database playground with sample data in seconds. It is a great way to test your database queries and learn about the database.

You can run a single command to setup playground dataset in PostgreSQL, MySQL, PostgreSQL and some sample indexes (omdb and shakespeare) in Elasticsearch.

# Usage

Make sure you have Docker installed and running.

## run all the services
docker-compose up -d

## run a single service
docker-compose up -d mongo

## clean up the playground
docker-compose down

# Database Credentials
Given below are the default configuration for the databases.

## PostgreSQL
Following are the details to connect to the database
`
Host:     localhost
Port:     6432
Username: admin
Password: admin
Database: playground
`
You can use the following command to run commands on the database
`
docker exec -it db_playground_postgres psql -U admin -d playground
`

## MySQL
Following are the details to connect to the database
`
Host:     localhost
Port:     4306
Username: admin
Password: admin
Database: playground
`
You can use the following command to run commands on the database
`
docker exec -it db_playground_mysql mysql -uadmin -padmin
`

# MongoDB
Following are the details to connect to MongoDB
`
Host:     localhost
Port:     37017
Database: playground
`
You can use the following command to run commands on the database
`
docker exec -it db_playground_mongo mongosh
`

# Elasticsearch
Following are the details to connect to Elasticsearch
`
Host:     localhost
Port:     9200
Indexes:  omdb, shakespear
`
You can use the following command to run commands on the container
`
docker exec -it db_playground_elasticsearch sh
`

# Redis
Following are the details to connect to Redis
`
Host:     localhost
Port:     6379
`
You can use the following command to run commands on the container
`
docker exec -it db_playground_redis redis-cli
`