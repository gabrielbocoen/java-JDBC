# Java e JDBC: Trabalhando com um banco de dados

Códigos fontes feitos durante o curso de Java e JDBC: Trabalhando com um banco de dados.

java.sql

Neste curso, aprendemos que (by João Victor):
- Para acessar o banco de dados, precisamos de um driver. Um driver nada mais é do que uma biblioteca (JAR);
- JDBC significa Java DataBase Conectivity. JDBC define uma camada de abstração entre a sua aplicação e o driver do banco de dados. Essa camada possui, na sua grande maioria, interfaces que o driver implementa;
- Para abrir uma conexão, devemos usar o método getConnection, da classe DriverManager. O método getConnection recebe uma string de conexão JDBC, que define a URL, usuário, senha, etc;
- Para simplificar e encapsular a criação da conexão, devemos usar uma classe ConnectionFactory. A classe ConnectionFactory segue o padrão de criação Factory Method. O Factory Method encapsula a criação de um objeto;
- Para executar um comando SQL, podemos usar a interface java.sql.Statement. O método execute envia o comando para o banco de dados. Dependendo do comando SQL, podemos recuperar a chave primária ou os registros selecionados.

