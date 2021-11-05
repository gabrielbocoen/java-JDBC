# Java e JDBC: Trabalhando com um banco de dados

Códigos fontes feitos durante o curso de Java e JDBC: Trabalhando com um banco de dados.

java.sql

Neste curso, aprendemos que (by João Victor):
- Para acessar o banco de dados, precisamos de um driver. Um driver nada mais é do que uma biblioteca (JAR);
- JDBC significa Java DataBase Conectivity. JDBC define uma camada de abstração entre a sua aplicação e o driver do banco de dados. Essa camada possui, na sua grande maioria, interfaces que o driver implementa;
- Para abrir uma conexão, devemos usar o método getConnection, da classe DriverManager. O método getConnection recebe uma string de conexão JDBC, que define a URL, usuário, senha, etc;
- Para simplificar e encapsular a criação da conexão, devemos usar uma classe ConnectionFactory. A classe ConnectionFactory segue o padrão de criação Factory Method. O Factory Method encapsula a criação de um objeto;
- Para executar um comando SQL, podemos usar a interface java.sql.Statement. O método execute envia o comando para o banco de dados. Dependendo do comando SQL, podemos recuperar a chave primária ou os registros selecionados;
- Ao executar SQL como Statement, temos um risco de segurança, chamado de SQL Injection. SQL Injection nada mais é do que passar um novo comando SQL como parâmetro;
- Para evitar SQL Injection, devemos usar a interface PreparedStatement. Diferentemente do Statement, o PreparedStatement trata (sanitiza) cada parâmetro do comando SQL;
- O banco de dados oferece um recurso chamado de <b>transação</b>, para juntar várias alterações como unidade de trabalho. Se uma alteração falha, nenhuma alteração é aplicada (é feito um <b>rollback</b> da transação). Todas as alterações precisam funcionar para serem aceitas (é feito um <b>commit</b>);
- <b>commit</b> e <b>rollback</b> são operações clássicas de transações;
- Para garantir o fechamento dos recursos, existe no Java uma cláusula <i>try-with-resources</i>. O recurso em questão deve usar a interface <b>Autoclosable</b>.
