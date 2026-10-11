# Práctica de integración continua con GitHub Actions

Este repositorio contiene un programa **Hola mundo** en JavaScript y un flujo de integración continua que envía una notificación a [ntfy.sh/devops-itla](https://ntfy.sh/devops-itla) después de cada `push` a la rama `main`.

## Archivos principales

- `hola-mundo.js`: programa solicitado.
- `.github/workflows/alerta.yml`: workflow de GitHub Actions.

## Ejecución local

Se necesita Node.js. Para ejecutar el programa:

```bash
node hola-mundo.js
```

Salida esperada:

```text
Hola, mundo desde GitHub Actions!
```

## Funcionamiento del workflow

Al subir código a `main`, GitHub Actions realiza estos pasos:

1. Descarga el repositorio.
2. Configura Node.js 20.
3. Ejecuta el programa Hola mundo.
4. Publica en `https://ntfy.sh/devops-itla` una notificación con el repositorio, la rama y el identificador del commit.
