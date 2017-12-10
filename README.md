# Supported tags and respective **Dockerfile** links	

---

- 1.0.0 ([*Dockerfile*](https://github.com/LucasBRamos/laravel-sqlsrv/blob/master/Dockerfile))

# Running Containers

---

To create the container, copy the code below and paste it into your docker-compose.yml.

The container has already been configured to recognize Laravel's  ```public``` folder, so just copy the root folder of your project to the ```/var/www``` folder of the container and your project already will be running.

```
version: '3'

services:
	app:
	    image: lucasramos/laravel-sqlsrv:1.0.0
	    container_name: container_name
	    network_mode: "bridge"
	    volumes:
	      - .:/var/www/
	    ports:
	      - "80:80"
```

# References

---

For the image configuration, I used the Dockerfile project [gjuniioor/php-sqlsrv](https://hub.docker.com/r/gjuniioor/php-sqlsrv/) and adapted it according to my needs to run the project Laravel.


# Changelog

---

- 1.0.0 - First version that allows to run Laravel project with connection to SQL Server database and generation of PDFs using the tool ```wkhtmltopdf```


# Bugs, Questions and Contribution

---

Has a bug found? Please, open a [Issue](https://github.com/LucasBRamos/laravel-sqlsrv/issues), a [Pull Request](https://github.com/LucasBRamos/laravel-sqlsrv/pulls) or contact me: [@LucasBRamos](https://github.com/LucasBRamos).