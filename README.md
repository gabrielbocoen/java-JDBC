# Java e JDBC: Trabalhando com um banco de dados

Códigos fontes feitos durante o curso de Java e JDBC: Trabalhando com um banco de dados.

java.sql

Neste curso, aprendemos que (by João Victor):
- Para acessar o banco de dados, precisamos de um <b><i>driver</i></b>. Um <i>driver</i> nada mais é do que uma biblioteca (JAR);
- <b>JDBC</b> significa <i>Java DataBase Conectivity</i>. JDBC define uma camada de abstração entre a sua aplicação e o <i>driver</i> do banco de dados. Essa camada possui, na sua grande maioria, interfaces que o <i>driver</i> implementa;
- Para abrir uma conexão, devemos usar o método <b>getConnection</b>, da classe <b>DriverManager</b>. O método <b>getConnection</b> recebe uma string de conexão JDBC, que define a URL, usuário, senha, etc;
- Para simplificar e encapsular a criação da conexão, devemos usar uma classe <b>ConnectionFactory</b>. A classe <b>ConnectionFactory</b> segue o padrão de criação <i>Factory Method</i>. O <i>Factory Method</i> encapsula a criação de um objeto;
- Para executar um comando SQL, podemos usar a interface <b>java.sql.Statement</b>. O método <b>execute</b> envia o comando para o banco de dados. Dependendo do comando SQL, podemos recuperar a chave primária ou os registros selecionados;
- Ao executar SQL como <b>Statement</b>, temos um risco de segurança, chamado de <b>SQL Injection</b>. <i>SQL Injection</i> nada mais é do que passar um novo comando SQL como parâmetro;
- Para evitar <i>SQL Injection</i>, devemos usar a interface <b>PreparedStatement</b>. Diferentemente do <b>Statement</b>, o <b>PreparedStatement</b> trata (sanitiza) cada parâmetro do comando SQL;
- O banco de dados oferece um recurso chamado de <b>transação</b>, para juntar várias alterações como unidade de trabalho. Se uma alteração falha, nenhuma alteração é aplicada (é feito um <b>rollback</b> da transação). Todas as alterações precisam funcionar para serem aceitas (é feito um <b>commit</b>);
- <b>commit</b> e <b>rollback</b> são operações clássicas de transações;
- Para garantir o fechamento dos recursos, existe no Java uma cláusula <i>try-with-resources</i>. O recurso em questão deve usar a interface <b>Autoclosable</b>;
- É boa prática usar um <b><i>pool</i> de conexões</b>;
- Um <i>pool</i> de conexões administra/controla a quantidade de conexões abertas. Normalmente tem um mínimo e máximo de conexões;
- Como existe uma interface que representa a conexão (<b>java.sql.Connection</b>), também existe uma interface que representa o <i>pool</i> de conexões (<b>javax.sql.DataSource</b>);
- <b>C3PO</b> é uma implementação Java de um <i>pool</i> de conexão;
- Para cada tabela de domínio, temos uma classe de domínio. Por exemplo, a tabela <b>produtos</b> tem uma classe <b>Produto</b> associada. Objetos dessa classe representa um registro na tabela;
- Para acessar a tabela, usaremos um padrão chamado <b><i>Data Access Object</i> (DAO)</b>. Para cada classe de domínio, existe um DAO. Por exemplo, a classe <b>Produto</b> possui um <b>ProdutoDao</b>. Todos os métodos JDBC relacionados com o produto devem estar encapsulados no <b>ProdutoDao</b>.
