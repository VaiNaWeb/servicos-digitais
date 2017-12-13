# Banco de dados

Um banco de dados ou base dados é uma coleção de dados relacionados entre si, como uma grande caixa em que armazenamos e organizamos todas as nossas informações de forma muito simples e inteligente. Cada banco de dados tem suas características e conceitos, mas geralmente todos são criados com o propósito de armazenar e organizar dados para que possamos acessar nossas informações de forma eficiente.

Vamos estudar um tipo de banco que chamamos de relacional, não se prenda nesse conceito agora, com o tempo isso vai ficar mais claro. Nesse banco, os dados são organizados em tabelas interligadas. Essas tabelas são formadas por linhas e colunas. 

Para trabalhar com as tabelas, usamos uma linguagem chamada SQL, que significa Linguagem de consulta estruturada. Basicamente, para criar novos bancos, novas tabelas, manipular dados de tabelas existentes, e mais algumas outras coisas, usamos comandos do SQL.

Vamos usar como exemplo nessa aula o FavelaFlix, uma aplicação fictícia que oferece serviços sobre o cinema produzido na favela. O FavelaFlix exibe uma lista de filmes que a pessoa pode assistir em casa através de sua plataforma. Através da nossa aplicação, consultas são feitas ao nosso banco de dados.

## Criando um banco de dados

O problema, é que nosso banco de dados não existe ainda, então vamos cria-lo! Para isso usamos o comando CREATE DATABASE, a sintaxe fica assim:

```
CREATE DATABASE FavelaFlix; 
```

## Criando uma tabela

Nosso banco precisa também de tabelas, onde armazenaremos nossos dados, vamos criar uma tabela que armazena os dados dos filmes. Precisamos armazenar em uma tabela os dados referentes ao titulo, genero e ano de cada filme, no SQL usamos o comando CREATE TABLE, a sintaxe completa fica assim:
```
CREATE TABLE filmes (
    titulo varchar(255),
    genero varchar(255),
    ano int
); 
```

Para identificar cada filme, precisamos adicionar um id, com a propriedade AUTO_INCREMENT, dessa forma o próprio banco de dados cria esse ID de forma automática. Outra propriedade que precisamos adicionar também é PRIMARY KEY, e adicionar a ela o valor da nossa chave primaria, geralmente o id, assim o id é a nossa primeira chave, que podemos usar para identificar cada filme.
```
CREATE TABLE filmes (
    id int AUTO_INCREMENT,
    titulo varchar(255),
    genero varchar(255),
    ano int,
    PRIMARY KEY (id)
); 
```
## Adicionando dados
```
INSERT INTO filmes (titulo, genero, ano)
VALUES ('Neguinho e Kika','Ficção', 2013);
```

## Selecionando dados

Para selecionar os dados, usamos o comando SELECT, e indicamos uma ou mais colunas e qual tabela queremos selecionar.
```
SELECT titulo FROM filmes;
```

É possível também ao invés de especificar as colunas, selecionar todas as colunas de uma tabela, para isso usamos o seletor universal * fica assim:
```
SELECT * FROM filmes;
```
