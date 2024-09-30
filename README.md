Banco de dados relacional: armazenamento de dados estruturados, organizados em tablelas, com linhas e colunos que se relacionam

O conceito vem de varias tabelas se relacionarem entre si
Ex: mysql, sql server, oracle

-------------------------------------------------------------------

Banco de dados não relacional: armazenamento não estruturados ou semi estruurados

Não estruturado: dados brutos

Semi estruturado: json
Ex: mongoDb

---------------------------------------------------------------
SQL Server

>create table Produtos (
	Id int identity(1,1) primary key not null, --// identity se encrementa
	Nome varchar(255) not null,
	cor varchar(50) null,
	Preco decimal(13,2) not null,
	Tamanho varchar(5) null,
	Genero char(1) null
)

>--select * from Clientes //selecionar tudo
--order by Nome desc //ordenar por nome e decrecente
--select Id, Nome, Sobrenome from Clientes
--where Nome ='Ken' or Nome='Rob' //filtro
--where Nome like 'R%' //comeca com R | %G% = todo mundo que tem G
--order by Nome, Sobrenome


>--insert into Clientes (Nome, Sobrenome, Email, AceitaComunicados, DataCadastro) //assim dá pra escolher a ordem das colunas
>--insert into Clientes values ('Maira', 'A', 'email.com', 1, GETDATE()) --//assim não dá pra mudar a ordem

>--select * from Clientes where nome = 'Maira'

>--update Clientes set Email ='email3@.com', AceitaComunicados=0 where Id=14 //atualizar, sempre com um filtro

>--select * from Clientes

>delete Clientes where Id=11 --//deletar

Primary key: chave que serve como indice
Foreingn key: é uma referencia de outra tabela, uma chave primaria de outra tabela

Identity faz o incremento automatico
