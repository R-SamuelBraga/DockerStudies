# DockerStudies
Explorando e estudando Docker

# Executando um container
-docker pull [image]
-docker run [image]
-docker stop [image]
-docker run -it [ubuntu]

# Executando aplicações no container
-docker run -dti [image]
-docker exec -it [id ou nome da image] /bin/bash

# Excluir e nomear containers
-docker stop [id]
-docker rm [id]
-docker rm [image]

-docker run -dti --name NameImage [image]

# Copiar arquivos da máquina para container
-docker cp arquivo.txt Ubuntu-A:/caminho/
# Copiando arquivos do container para máquina
-docker cp Ubuntu-A:/caminho/arquivo.txt NomeCopia.txt

# Instalar container Mysql
-docker pull mysql
# Configurando senhas e porta mysql
-docker run --help
- docker run -e MYSQL_ROOT_PASSWORD=123456 --name mysql-A -d -p 3306:3306 mysql
# Acessando Bash mysql sem mysqlclient
-docker exec -it mysql-A bash
# Acessando root mysql
-mysql -u root -p --protocol=tcp
aparecerá  ->password:
# Instalando mysqlclient
- apt -y install mysql-client


