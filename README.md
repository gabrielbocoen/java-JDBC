# Java e JDBC: Trabalhando com um banco de dados

Códigos fontes feitos durante o curso de Java e JDBC: Trabalhando com um banco de dados.

java.sql

Neste curso, aprendemos que (by João Victor):
- Para acessar o banco de dados, precisamos de um driver. Um driver nada mais é do que uma biblioteca (JAR);
- JDBC significa Java DataBase Conectivity. JDBC define uma camada de abstração entre a sua aplicação e o driver do banco de dados. Essa camada possui, na sua grande maioria, interfaces que o driver implementa;
- Para abrir uma conexão, devemos usar o método getConnection, da classe DriverManager. O método getConnection recebe uma string de conexão JDBC, que define a URL, usuário, senha, etc.
