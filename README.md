### Introduction

GildedRoseVM is a full PHP development environment for Docker.

    PHP versions: 8.0

### Requirements

    Docker [ >= 20.10 ]

### Quick Overview

Let’s see how easy it is to set up our demo stack `PHP` `Nginx` & `Composer`

1 - Clone GildedRoseVM inside your PHP project:

```
git clone https://github.com/TienDang2802/GildedRoseVM.git
```

2 - Enter the GildedRoseVM folder and rename `.env.dist` to `.env`.

```
cp .env.dist .env
```

You can edit the `.env` file to choose which software’s you want to be installed in your environment. You can always refer to the `docker-compose.yml` file to see how those variables are being used.

At the top, change the `APP_CODE_PATH_HOST` variable to your project path.

```
APP_CODE_PATH_HOST=../gilded-rose-project
```

Make sure to replace `gilded-rose-project` with your project folder name.

3 - Build the environment and run it using:

```
docker compose up -d
```

4 - Enter the Workspace container, to execute commands like (Composer, PHPUnit …)

```
docker exec -it {workspace-container-id} bash
```

5 - Open your browser and visit your localhost address.

Make sure you add use the right port number as provided by your running server.

```
http://127.0.0.1
```