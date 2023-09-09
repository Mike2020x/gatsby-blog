---
layout: blog
title: Comandos útiles para Docker
date: '2023-09-09T11:44:15-05:00'
thumbnail: /assets/images/images.png
rating: '4'
---
#### Lista de imágenes

```
$ docker image ls
```

#### Elimina una imagen específica

```
$ docker image rm [nombre de la imagen]
```

#### Elimina todas las imágenes existentes

```
$ docker image rm $(docker images -a -q)
```
#### Lista todos los contenedores existentes (en funcionamiento y no en funcionamiento)

```
$ docker ps -a
```

#### Detener un contenedor específico

```
$ docker stop [nombre del contenedor]
```

#### Detener todos los contenedores en funcionamiento

```
$ docker stop $(docker ps -a -q)
```

#### Elimina un contenedor específico (solo si está detenido)

```
$ docker rm [nombre del contenedor]
```

#### Elimina todos los contenedores (solo si están detenidos)

```
$ docker rm $(docker ps -a -q)
```

#### Mostrar los registros de un contenedor

```
$ docker logs [nombre del contenedor]
```
