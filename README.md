# SchoolOfNet_Iniciando_ASPNet_CORE_Autenticacao_Identity
ASP.NET Core - AutenticaÃ§Ã£o com Identity

Para criar um projeto com Identity deve :
  dotnet new mvc --auth Individual --use-local-db

Adicionar a dependecia para acesso ao banco de dados MySQL:
dotnet add package Pomelo.EntityFrameworkCore.MySql --version 2.2.0

Após executar o restore para atualizar as depedencias:
dotnet restore

Criar o banco de dados:
CREATE DATABASE `netcoreidentity` /*!40100 COLLATE 'latin1_general_cs' */;

O Identity já cria os migrations responsáveis por criar as suas tabelas.
Para aplicar a migração deve executar:
```
dotnet ef database update
```
OBS: A aplicação não deve estar rodando para executar este comando.

#Algumas tabelas que são criadas:
| Nome| Descrição|
|-----|----------|
|AspNetUsers| Tabela de usuários|
|AspNetUserClaims|Campos personalisados do usuário|

