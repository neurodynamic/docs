## Contenedor Docker para Volt

Crea un Dockerfile en tu aplicación de Volt con lo siguiente:

```
FROM otzy007/voltframework
```

Luego de esto puedes crear tu imagen de Docker

```
FROM otzy007/voltframework
```

Y correrlo:

```
docker run --name my-volt-app -p 3000:3000 -d my-volt-app
```

Ahora ya puedes ver tu aplicación en esta direccion: http://localhost:3000
