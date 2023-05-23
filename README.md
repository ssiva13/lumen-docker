# Setting Lumen in Docker

## Initial set up

- Build Container

  ```bash
  docker compose up -d
  ```

- Open container in your terminal or cmd

  ```bash
   docker exec -it lumen-api /bin/bash
  ```

- Install Laravel Lumen project shell from the container terminal

  ```bash
  composer create-project --prefer-dist laravel/lumen .
  ```
  
- Go to `http://localhost:8800/` in your browser
- Open the project in your preferred editor - your project is now available in the `code` directory.
  
**Note** - Feel free to change the mysql variables to values of your choice

```yaml
    environment:
      - MYSQL_ROOT_PASSWORD=secret
      - MYSQL_DATABASE=default
      - MYSQL_USER=myuser
      - MYSQL_PASSWORD=myuser
```

**Note** - Feel free to change the container arguments

```yaml
      args:
        user: user
        uid: 1000
```

- For more instructions go to [Laravel Lumen](https://lumen.laravel.com/)
