# How to run 

1) copy the repo or just docker-compose.yml
2) create  .env file and add fields according to your need. use keys from env-example file
3) install docker 
4) run the following command
  ```
 
   $ docker compose   up -d  //in detached mode with terminal

   $ docker compose up //with interaction mode
  ```

5) Run migrations once

    a) ``` docker ps ```

    select the container id corresponds to web

    b)  $ ``` docker exec -it <container id> bash ```

    $ ```python3 manage.py makemigrations```

    $ ```python3 manage.py migrate ```

6) create superuser account
 ```
   $ python3 manage.py createsuperuser
   ```
   provide username,email,password

7) check application working properly in http://localhost/ and admin portal at http://localhost/admin   
