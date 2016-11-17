# arify

## Usage

1. On your host, copy env-example.txt to a file named .env 

```
$ cp env-example.txt .env
```

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
