¿Que es un contenedor?
Forma de empaquetar una aplicacion con todas las dependencias incluyendo sus archivos de configuracion

Los contenedores son portables y por consiguiente facil de compartir entrre los desarrolladores y las operaciones
Haciendo el despliegue y desarrollo mas facil

¿Donde se almacenan?
Repositorio de contenedores: Similar a github
Existen dos tipos:
Privados
Publicos: Docker Hub -> se encuentran aplicaciones como pythom, nodejs, postgres, python, mysql, golang

¿Que habia antes de los contenedores?
Cada persona tenia su propio computador con diferentes sistemas operativos y versiones de software
Cada persona debia de preparar su computador con todas las dependencias necesarias para poder trabajar
Lo que probocaba
Dificil de compartir el trabajo con otros desarrolladores
Dificil de replicar el ambiente de desarrollo en otros computadores

Con contenedores
Descargar una imagen basa en un sistema operativo

Despliegue sin contenedores
NEcesitamos el codigo de la aplicacion
las instruccioneas para actualizar las dependencias
archivos de configuaciones
esto se debe enviar al equipo de operaciones
Deben actualizar las libreria de los servidores o levantar mas servidores
Este proceso puede provocar errores
En distitnas versiones de dependencias y problemas en la comunicacion
y si hay errroes deben realizarce roolback: regresar a la version anterior

Con contenedores
Los devs y ops pueden trabajar juntos para crear una imagen de la aplicacion, que contiene todo lo necesario para ejecutar la aplicacion
La unica dependecia que necesita esa imagen, es el runtime de docker
todo este proceso se puede automatizar con pipeleines de CI/CD


¿Que es una imagen?
Es un paquete que contiene todo lo necesario para ejecutar una aplicacion
Dependencias, codigo, lo que se comparte

¿Que es un contenedor?
Son capas de imagenes 
La primera capa, mas utilizada es slpine linux, por ser la mas liviana
Luego hay muchas imagines hasta llegar a la capa de aplicacion
Los contenedores pesan poco!!!

Comparacion con maquinas virtuales
Las maquinas virtuales son mas pesadas, ya que contienen un sistema operativo completo
Los contenedores comparten el mismo kernel del sistema operativo
Por lo que son mas livianos

docker vs maquinas virtuales

En que consiste la virtualkizacion?
En 3 capas
Hardware: Servidor fisico
Kernel: Sistema operativo
Aplicacion: Aplicacion que se ejecuta en el sistema operativo

Cuando trabajamos con maquinas virtuales, trabajamos con el kernel y las aplicaciones, haciendo que las maquinas virtuales sean mas pesadas

En cambio docker, lo que se virtualiza es la capa de aplicaciones, y el kernel utiliza el del sistema operativo, haciendo que los contenedores sean mas livianos

Existen 3 tipos de virtualkiacion
1. Para Virtualizaciones:
* Host (sistema operativo anfitrion) y SO invitado (sisitema operativo virtualizado)
Intenta entregan la mayor cantidad de acceso por parte Host, de su hardwarew al SO invitado
2. Virtualizacion parcial:
Donde algunos componentes del hardware se virtualizan para el so cliente
3. Virtualizacion completa:
Donde se virtualiza todo el hardware, y el SO cliente no tiene acceso directo al hardware

Para todos estso casos docker es superior
POrque utiliza directamente el kernel del sistema operativo
Y no necesita de un sistema operativo virtualizado
* Las imagenes de docker son mas livianas
* Los contenedores de docker son mas rapidos

¿Que es Docker?
Docker es una plataforma de software que permite a los desarrolladores, administradores de sistemas y arquitectos de aplicaciones crear, probar e implementar aplicaciones de manera eficiente y segura en contenedores. Los contenedores permiten a un desarrollador empaquetar una aplicación con todas las partes necesarias, como bibliotecas y otras dependencias, y enviarla como una sola imagen. Al hacerlo, el desarrollador puede estar seguro de que la aplicación se ejecutará en cualquier otro entorno de Docker, independientemente de las diferencias en la infraestructura subyacente.