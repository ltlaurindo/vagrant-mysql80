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


CREATE DATABASE LTLVagrant;
USE LTLVagrant;
CREATE TABLE Trabalho (
  ID mediumint(8) unsigned NOT NULL auto_increment, 
 materia varchar(100),
  nomeProfessor varchar(100),
  nota char(3)
  PRIMARY KEY (`ID`) 
 ) AUTO_INCREMENT=1; 

 teste lilian


INSERT INTO Exercicio (materia,descricao,nomeProfessor,nota) VALUES ('Infrastructure and Cloud Computing','Joao Henrique','10');


