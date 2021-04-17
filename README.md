# MBA - Engenharia de Software
# Prof - João Henrique 
# Aula: Infrastructure and Cloud Computing


##### Box Utilizada
##### Nome: jitendradpatel/mysql-8

##### Versão: 1.0

##### Descrição da VM utilizada: Debian GNU/Linux 9 (stretch)

##### Descriçao do SGBD: mysql  Ver 8.0.12 for Linux on x86_64 (MySQL ##### Community Server - GPL)

##### Para mais detalhes sobre a box, acesse:
##### https://app.vagrantup.com/jitendradpatel/boxes/mysql-8

1. Passo a passo: 
2. Faça o donwload do repositório: https://github.com/ltlaurindo/vagrant-mysql80.git


3. Para inicializar a maquina virtual execute o comando abaixo:
4. vagrant up

5. Execute o comando abaixo para acessar a maquina virtual via ssh
6. vagrant ssh mysql

7. Execute o comando para entrar logar no Mysql via:
8. mysql -u root -p

9. Informe a senha
10. root

11. Execute os comandos a seguir para criar um banco de dados:


CREATE DATABASE LTLVagrant;
USE LTLVagrant;
CREATE TABLE Trabalho (
  ID mediumint(8) unsigned NOT NULL auto_increment,
  materia varchar(100),
  nomeProfessor varchar(100),
  nota char(3)
  PRIMARY KEY (`ID`)
) AUTO_INCREMENT=1;

INSERT INTO Exercicio (materia,descricao,nomeProfessor,nota) VALUES ('Infrastructure and Cloud Computing','Joao Henrique','10');


