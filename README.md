# SustainableEnv

[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/koiusa/SustainableEnv)](https://github.com/koiusa/SustainableEnv/graphs/commit-activity)
[![GitHub issues](https://img.shields.io/github/issues/koiusa/SustainableEnv)](https://github.com/koiusa/SustainableEnv/issues)
[![GitHub license](https://img.shields.io/github/license/koiusa/SustainableEnv)](https://github.com/koiusa/SustainableEnv/blob/main/LICENSE)

Work support server environment

## Verified architecture

```shell
$ cat /etc/os-release
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=24.04
DISTRIB_CODENAME=noble
DISTRIB_DESCRIPTION="Ubuntu 24.04.1 LTS"
```

```shell
$ arch
x86_64
```

## overview

- [gitbucket](https://github.com/gitbucket/gitbucket)  
   source management server

- [jenkins](https://www.jenkins.io)  
   automation suport server

- [redmine](https://www.redmine.org/projects/redmine/wiki)  
   project management server

- [ums](https://www.universalmediaserver.com)  
   media server

- [wireguredEasy](https://github.com/wg-easy/wg-easy)  
   vpn server

## How to use

### environment construction

- Dependency environment installation

    Use this task command only when building the environment.
    ```sh:install the docker engine
        $ sudo ./setup.sh
    ```
    ```sh:add user to docker group
        $ sudo usermod -aG docker $USER
    ```
### Contaner controll

- Container startup

    Run this task at each service startup.
    ```sh:change current directory
        $ cd docker/[anyServiceDir]
    ```
    ```sh:start up docker container
        $ docker compose up -d
    ```

- Container shutdown

    Run this task at each service startup.
    ```sh:change current directory
        $ cd docker/[anyServiceDir]
    ```
    ```sh:start up docker container
        $ docker compose down
    ```

- Container restart

    Run this task at each service startup.
    ```sh:change current directory
        $ cd docker/[anyServiceDir]
    ```
    ```sh:start up docker container
        $ docker compose restart
    ```

## Container Setup
- Setup each service
    Please refer to README in details for each docker directory.
    ```sh:view redme file
        $ cat docker/[anyServiceDir]/README.md
    ```
