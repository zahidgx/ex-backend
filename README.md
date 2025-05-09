﻿# Backend app_flask EC2

 El backend del proyecto está desarrollado con Flask, un microframework de Python que permite crear aplicaciones web ligeras y eficientes. Este backend se encarga de manejar la lógica de negocio, las operaciones con la base de datos y la comunicación con el frontend mediante una API RESTful.

# Despliegue en Servidor EC2
La aplicación está desplegada en una instancia EC2 de Amazon Web Services (AWS), lo que permite que esté disponible desde internet y cuente con una infraestructura flexible y escalable para producción.

# Configuración de Producción
Servidor WSGI: Gunicorn
Gunicorn se utiliza como servidor WSGI para ejecutar la aplicación Flask, permitiendo manejar múltiples procesos y mejorar el rendimiento general.

# Servidor Proxy Reverso: Nginx
Nginx actúa como proxy reverso, redirigiendo las peticiones al servidor Gunicorn y gestionando aspectos como la carga, los archivos estáticos y la seguridad.

# Base de Datos en la Nube
Para el almacenamiento de datos, se configuró una base de datos MySQL utilizando Amazon RDS (Relational Database Service).
El backend se conecta a esta base de datos mediante credenciales seguras, lo que permite una administración centralizada, copias de seguridad automáticas y alta disponibilidad sin necesidad de gestionar la infraestructura de base de datos manualmente.

# Seguridad
La configuración incluye un certificado SSL (autofirmado o de una autoridad certificadora) para habilitar HTTPS y proteger la comunicación entre cliente y servidor.

# Funcionalidad Principal de la API
El backend expone una ruta principal bajo el prefijo /api:

/users/: Permite crear, editar y eliminar usuarios. También incluye funciones de autenticación y consulta de información de usuarios registrados.

# Tecnologías y Componentes
Framework: Flask

Base de datos: MySQL alojada en Amazon RDS

Autenticación: (JWT, sesiones, etc., si aplica)

Despliegue: AWS EC2 + Gunicorn + Nginx

Comunicación: API RESTful
