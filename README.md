# arify

## Usage

It's good practice to not include user credentials inside the `docker-compose.yml` file, so we'll group them in an `.env` file from which docker-compose will fetch them. 

### Setup Docker containers

1. Clone this repository. 
1. Create a file named .`env` by copying `.env_example`:

    ```
    $ cp .env_example .env
    ```

1. Populate this new `.env` file with your own credentials. Make sure `.env` is in the same directory as `docker-compose.yml`.
1. Start up the Docker containers:

    ```
    $ (source .env && docker-compose up -d)
    ```

### Setup ownCloud

Open your browser to domain.com:7070 (or to whatever value you've changed `OWNCLOUD_PORT` to in your `.env` file. Then follow these steps to setup your ownCloud installation:
 
1. Select _Storage & database_ --> _Configure the database_ --> _MySQL/MariaDB_  
1. Database user: `root`
1. Database password: put the value of `MYSQL_ROOT_PASSWORD` in your `.env` file
1. Database name: pick any name
1. Database host: replace `localhost` with the name of the container containing ownCloud's database (`arify_db` in this case) 
