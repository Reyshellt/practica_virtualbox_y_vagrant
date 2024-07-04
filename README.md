# Proyecto de Servidor Web con Vagrant y VirtualBox

Este proyecto configura dos máquinas virtuales utilizando Vagrant y VirtualBox, instala el servidor web Apache en ambas, y comparte una carpeta local con el directorio de Apache en cada máquina.

## Prerrequisitos

Asegúrate de tener instalados los siguientes programas en tu sistema:

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Configuración del Proyecto

1. Clona este repositorio en tu máquina local:
    ```sh
    git clone https://github.com/tuusuario/tu-repositorio.git
    cd tu-repositorio
    ```

2. Crea una carpeta llamada `html` en el directorio raíz del proyecto. Esta carpeta contendrá tus archivos HTML que serán servidos por Apache:
    ```sh
    mkdir html
    ```

3. Coloca tus archivos HTML dentro de la carpeta `html`. Por ejemplo, puedes crear un archivo `index.html`:
    ```html
    <!DOCTYPE html>
    <html>
    <head>
        <title>Mi Servidor Web</title>
    </head>
    <body>
        <h1>¡Hola desde Apache en Vagrant!</h1>
    </body>
    </html>
    ```

## Inicio de las Máquinas Virtuales

Para iniciar las máquinas virtuales, navega al directorio del proyecto y ejecuta el siguiente comando:

```sh
vagrant up
