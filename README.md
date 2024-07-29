﻿# MarvelAppFullStack

Antes de empezar debe chequear que tienes una versión de NodeJS igual o superior  a la 20.7.0 (hazlo con el comando "node -v") y una versión de NPM igual o superior a la 10.8.2 (hazlo con el comando "npm -v"), también es mandatorio contar con SQL Server 2022 y Docker 


1. Ir al Linkl (https://github.com/Bushogun/MarvelAppFullStack/archive/refs/heads/main.zip)
2. Click derecho -> Extract here
3. Abrir folder en Visual Studio Code
4. Aber un nuevo terminal (ctrl + shift + ñ)
5. Corre el comando "cd backend"
6. Corre el comando "npm i"
7. Inicia Docker
8. Corre el comando "docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=yourStrong#Password" -p 1433:1433 -d mcr.microsoft.com/mssql/server:2022-latest"
9. Corre el SQL llamado "db.sql" ubicado en Backend -> database -> db.sql creando una conexión a esa base de datos, puede usar el usuario "sa" con la clave "yourStrong#Password" usando SQL Server Management Studio o con una extensión de Visual Studio Code llamada SQL Server (mssql)
10. Corre el comando "npm run dev"
11. Inicia una nueva terminal (ctrl + shift + ñ)
12. Corre el comando "cd frontend"
13. Corre el comando "npm i"
14. Corre el comando "npm run dev"

RECUERDA SIEMPRE CERRAR SESIÓN PARA NO TENER ERROES EN FUTURAS EJECUCIONES!

<p align="right">
  <img src="https://media.giphy.com/media/SvFocn0wNMx0iv2rYz/giphy.gif" alt="GIF Animado">
</p>

Esta prueba fue realizada en tiempo récord con una arquitectura Hexagonal en el backend orientado al desarrollo con DDD y programación funcional en el front y cuenta con funcionalidades como:
Base de datos la cual persiste el usuario, cómics favoritos, y cómics
Los cómics se registran por Id y Título 
Pantalla de LogIn
Hace login y almacena un token que permite la interacción con el backend el cual controla las peticiones al API de Marvel y controla las funcionalidades de la aplicación 
Sin un login no se puede acceder a rutas protegidas como lo es el "Dashboard" y los comics específicos a los que se quiere ver los detalles
LogIn con token JWT el cuál es persistido en el estado de Redux cuya configuración almacena en un localStorage 
Pantalla de Register
Comprueba si existe el usuario que se va a registrar por medio de su Identificación y su correo
Maneja el formulario de registro con validación de campos con la librería de React Form
Tanto el front como el Backend poseen un sistema de verificación de formulario y datos enviados
Sistema para añadir cómics favoritos y obtener cómics favoritos de usuarios específicos
En el backend se encripta la llave con la que se hacen las solicitudes al api de Marvel 
En el front no se usaron librerías de diseños predefinidos, sino que cada línea de CSS fue escrita como parte de un reto personal
Una vez iniciada sesión se obtiene el usuario y se despliega su nombre en un componente el cual despliega la acción de cerrar sesión.
