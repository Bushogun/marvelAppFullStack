# MarvelAppFullStack

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
