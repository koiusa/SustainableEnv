## Security measures
- Please change your password from time to time to improve security.



## Change the database connection destination from the default to postgres, which is synchronized and started using Dockercompose.

```sh
$ docker ps
84eb3d1d2adb   postgres                               "docker-entrypoint.s…"   2 weeks ago   Up 2 weeks   5432/tcp, 0.0.0.0:5433->5433/tcp, :::5433->5433/tcp
                                                                     gitbucket-db
```

```sh:docker/gitbucket
$ cat ./data/database.conf
db {
  url = "jdbc:postgresql://gitbucket-db:5433/gitbucket"
  user = "sa"
  password = "sa"
#  connectionTimeout = 30000
#  idleTimeout = 600000
#  maxLifetime = 1800000
#  minimumIdle = 10
#  maximumPoolSize = 10
}
```

