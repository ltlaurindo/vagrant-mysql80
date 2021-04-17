#### MBA - Engenharia de Software
#### Prof - João Henrique 
#### Aula: Infrastructure and Cloud Computing

##### Exercicio:
###### Subir uma máquina virtual, usando Vagrant, com MySQL instalado e que esteja acessível no host da máquina na porta 3306. Enviar a URL Github do código. Atividade individual ou em grupo, vocês que definem.

##### **Box Utilizada:**
Nome: jitendradpatel/mysql-8

##### **Versão:** 
 1.0

##### **Descrição da VM utilizada:** 
Debian GNU/Linux 9 (stretch)

##### **Descriçao do SGBD:**
mysql  Ver 8.0.12 for Linux on x86_64 (MySQLCommunity Server - GPL)

##### **Para mais detalhes sobre a box, acesse:**
https://app.vagrantup.com/jitendradpatel/boxes/mysql-8

##### **Passo a passo:**

1. Faça o donwload do repositório: 
> https://github.com/ltlaurindo/vagrant-mysql80.git


2. Para inicializar a maquina virtual execute o comando abaixo:
> vagrant up

3. Execute o comando a seguir para acessar a maquina virtual via ssh
> vagrant ssh mysql 

4. Execute o comando para entrar  no Mysql:
> mysql -u root -p 

5. Informe a senha:
> root
 
6. Execute os comandos a seguir para criar um banco de dados:


CREATE DATABASE MBA_2021;
USE MBA_2021;


CREATE TABLE EXERCICIOS
(
	COD_EXERCICIO			int						identity				primary key,
	NOME_MATERIA			nvarchar(50)			not null				unique,
	NOME_PROFESSOR			nvarchar(50)			not null				unique,
	PRAZO_ENTREGA			DATE		     	not null,
	STATUS					char(08)				not null
);

INSERT INTO EXERCICIOS
VALUES ('Coordenação de Curso', 'Marcus Vinicius Almeida Silva','12/04/2021','ENTREGUE'),
('Workshop de Abertura On-line', 'Angela Valiera','12/04/2021','ENTREGUE'),
('Infrastructure and Cloud Computing', 'Joao Henrique Victorino da Silva','14/04/2021','PENDENTE');


SELECT * FROM EXERCICIOS;




