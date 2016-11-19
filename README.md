# arify

## Usage

Create a file named .`env` by copying `.env_example`:

```
$ cp .env_example .env
```

Populate this new `.env` file with your own credentials. 

Make sure `.env` is in the same directory as `docker-compose.yml`.

Start up the docker containers:

```
$ (source .env && docker-compose up -d)
```


### Setup ownCloud

During initial ownCloud setup:

1. Select "Storage & database" --> "Configure the database" --> "MySQL/MariaDB"  
1. Database user: `root`
1. Database password: put the value of `MYSQL_ROOT_PASSWORD` in your `.env` file
1. Database name: pick any name
1. Database host: replace `localhost` with the name of the container containing ownCloud's database (`arify_db` in this case) 
