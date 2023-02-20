Docker project: cluster

Creating Swarm cluster with Vagrant

Descrição
Neste desafio de projeto iremos criar um Cluster Swarm local, utilizando máquinas virtuais, além, de aplicar nossos conhecimentos em Vagrant. Também vamos aprender uma forma de evitar as implementações manualmente, melhorando o desempenho dos desenvolvedores.

PASSO A PASSO:

Criar um Vagrantfile com as definições de 4 máquinas virtuais. Sendo uma máquina com o nome de master e as outras com os nomes de node01, node02 e node03; 
Cada máquina virtual deverá ter um IP fixo; 
Todas as MV deverão possuir o Docker pré-instalado; 
A máquina com o nome de master deverá ser o nó manager do cluster. 
As demais máquinas deverão ser incluídas no cluster Swarm como Workers. (Capturar serial para gerar um comando e incluir essa maquina no cluster)
Agora é a sua vez de ser o protagonista! Implemente o desafio sugerido pelo expert e suba seu projeto para um repositório próprio, com isso, você aumentará ainda mais seu portfólio de projetos no GitHub!

Pré-requisitos:

Conhecimento Básico em Docker(Cluster Swarm);
Conhecimento Básico em Git e GitHub;
Computador com SO de sua preferência(Windows, Linux, Mac OS);


## Step by Step Solution

Inside the work directory, insert all 4 files needed for this project;

Via terminal:

- Access the directory `cd ./docker-projeto2-cluster`

- Check the files in an editor `code .`

  It is possible insert more nodes, but the final ips cannot be duplicated
  
  Note: if the machine is master, it will run a specific script for masters `master.sh`; if not, it will run another script;
  
  Attention: In `master.sh` we generate a file called `worker.sh` with the serial needed through the command `sudo docker swarm join-token worker | grep docker > /vagrant/worker.sh - initially, this `worker.sh` file should be empty
  
- Commands

  `vagrant up` -> to up all virtual machines
  
  `vagrant ssh master` -> `sudo su` -> `docker node ls`
  
  With that, everything is done to create the cluster.
  
  To think about: Is that possible pre-install any image? And what about up some container? What about create a volume? A file? 




