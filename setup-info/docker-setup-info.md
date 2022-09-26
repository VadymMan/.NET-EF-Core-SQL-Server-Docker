init mssql server db image, create container, run container:
docker run -it -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=A&VeryComplex123Password" -p 1488:1488 --name sql-server-2022 mcr.microsoft.com/mssql/server:2022-latest

if mssql server db container is created, run this:
docker start -i sql-server-2022

mssql server db dockerhub images: https://hub.docker.com/_/microsoft-mssql-server