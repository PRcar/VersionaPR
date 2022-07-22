# Atividade 2

 - Criação de uma máquina virtual com as mesmas configuraçào da primeira atividade através do VMBox:
![179999631-0214a00e-7d24-49d8-b021-71c417130e41](https://user-images.githubusercontent.com/109623573/180073966-bc539089-2d69-4d9e-b7b4-8962e44ff632.png)

# Ajustando a primeira máquina virtual para conexão via SSH e configurações de rede:

 ### Ajustando DNS:

 - Editar o arquivo hosts do Windows e do Linux, adicionando a linha: 192.168.1.2 elklabmonitoriacontainer

# Ajustar de rede:
![Captura de tela Enpos3](https://user-images.githubusercontent.com/109623573/180086665-b7f724e3-d8a4-4e56-b283-f4bd59e7c582.png)

# Ajustando a segunda máquina virtual para conexão via SSH e configurações de rede:

### Ajustando DNS:

 - Editar o arquivo hosts do Windows e do Linux, adicionando a linha: 192.168.1.3 elklabmonitoriacontainer

# Ajustar de rede:
![Capturar](https://user-images.githubusercontent.com/109623573/180090148-47ffce15-d0dd-4101-9b81-afbed00e3068.PNG)

# Mudar a rede das duas VM'S de modo NAT para BRIDGE no VMBox:
![180000178-457ad7bd-df74-424d-ab98-f1563503f5e3](https://user-images.githubusercontent.com/109623573/180090593-13465968-5d57-4201-bf80-59bd8616540b.png)

# Criar relação de confiança entre as duas VMs:

# VM1: 

Criação das chaves:
- ssh-keygen 
- chaves armazenadas em /home/plinux/.ssh/

![image](https://user-images.githubusercontent.com/109623573/180438841-d397822b-4b0e-45ff-992b-396757796872.png)

- adicionar o IP da VM2 no arquivo hosts da VM1, para que haja conexão ssh via DNS na questão de relaçao de confiança:

![image](https://user-images.githubusercontent.com/109623573/180439483-0dcf6ffe-6db6-4e25-a72a-4547befa24fd.png)


# VM2:

- Adicionando o IP da VM1 no arquivo hosts da VM2, para que haja conexão via DNS na questão de relação de confiança e importação de chave: 

![image](https://user-images.githubusercontent.com/109623573/180441933-19cef33d-26ac-4fe2-a87d-64e0a383d3d2.png)

- importar a chave pública da VM1 para VM2, criando o arquivo authorized_keys para validação da chave com o comando:  scp id_rsa.pub plinux2@192.168.1.2:~/.ssh/authorized_keys

- configurar as permissões do arquivo authentication_keys, para que seja gravável apenas pelo usuário Plinux2, porém execultável pelo usuário, com o comando: chmod  700 ~/.shh/authorized_keys

![image](https://user-images.githubusercontent.com/109623573/180444231-a27b192d-ad85-4c2d-9928-e4db97521b3d.png)

