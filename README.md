# SchoolOfNet_Iniciando_ASPNet_CORE_Autenticacao_Identity
ASP.NET Core - Autenticação com Identity

Para criar um projeto com Identity deve :
  dotnet new mvc --auth Individual --use-local-db

Adicionar a dependecia para acesso ao banco de dados MySQL:
dotnet add package Pomelo.EntityFrameworkCore.MySql --version 2.2.0

Ap�s executar o restore para atualizar as depedencias:
dotnet restore

Criar o banco de dados:
CREATE DATABASE `netcoreidentity` /*!40100 COLLATE 'latin1_general_cs' */;

