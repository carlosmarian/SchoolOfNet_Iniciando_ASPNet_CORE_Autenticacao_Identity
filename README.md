# SchoolOfNet_Iniciando_ASPNet_CORE_Autenticacao_Identity
ASP.NET Core - Autenticação com Identity

Para criar um projeto com Identity deve :
```
  dotnet new mvc --auth Individual --use-local-db
```

Adicionar a dependecia para acesso ao banco de dados MySQL:
```
dotnet add package Pomelo.EntityFrameworkCore.MySql --version 2.2.0
```

Ap�s executar o restore para atualizar as depedencias:
```
dotnet restore
```

Criar o banco de dados:

CREATE DATABASE `netcoreidentity` /*!40100 COLLATE 'latin1_general_cs' */;

O Identity j� cria os migrations respons�veis por criar as suas tabelas.

Para aplicar a migra��o deve executar:
```
dotnet ef database update
```
OBS: A aplica��o n�o deve estar rodando para executar este comando.

#Algumas tabelas que s�o criadas:

| Nome| Descri��o|
|-----|----------|
|AspNetUsers| Tabela de usu�rios|
|AspNetUserClaims|Campos personalisados do usu�rio|


Para alterar a interface das telas do Identity, deve usado o code-Generator:
```
dotnet tool install -g dotnet-aspnet-codegenerator
```
Adicionar o Pacote "CodeGeneration.Design" ao projeto:
```
 dotnet add package Microsoft.VisualStudio.Web.CodeGeneration.Design
```
OBS: Por garantia executar um restore dos pacotes:
```
dotnet restore
```

Listar os arquivos que podem ser gerados para o Identity:
```
dotnet aspnet-codegenerator identity --listFiles
```

Para criar um arquivo, deve:

dotnet aspnet-codegenerator identity -dc < Arquivo de contexto da aplica��o > --files < Arquivos que desejo gerar >

```
dotnet aspnet-codegenerator identity -dc NetCOREAutenticacaoIdentity.Data.ApplicationDbContext --files Account.Register
```
Os arquivos ser�o gerados em:  .\Areas\Identity\Pages\Account

