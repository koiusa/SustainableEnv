## Security measures
- Please change your password from time to time to improve security.

## Troubleshooting
- If the service repeatedly restarts after starting the service, the database may not have been created in the container.
Please run the setup script. 

```sh
$ docker ps -a
cef6d256bd3d   postgres:15.0                          "docker-entrypoint.s…"   2 weeks ago   Up 2 weeks   5432/tcp
                                                                     redmine-redmine-db-1
```

```sh
$ ./setup_postgres.sh redmine-redmine-db-1
```
