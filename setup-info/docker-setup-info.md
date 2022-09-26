init mssql server db image, create container, run container:
docker run -it -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=Carefusion1!" -p 1433:1433 --name sql-server-2022 mcr.microsoft.com/mssql/server:2022-latest

if mssql server db container is created, run this:
docker start -i sql-server-2022

mssql server db dockerhub images: https://hub.docker.com/_/microsoft-mssql-server

hints: if there is a login error in docker/app(EF) check another instance of SQL Server in the host-OS environment and be sure, the SA'a password is not predefined somewhere.