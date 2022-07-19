# Atividade Compass
Este é um projeto desenvolvido por estagiários na rede UOL Compass, no qual possui várias etapas a serem concluidas, utilizando projetos de redes, docker e etc.

Atividade 1:

Instalação da máquina virtual utilizando o VMBox, com um sistema Oracle Linux 8.6.

Configuração da máquina:

RAM: 4096mb
DISCO: 40gb
Hostname: elklabmonitoriacontainer
Configuração de disco:

Swap - 4gb --> swap
/boot/efi - 512mb --> EFI system
/boot - 1024mb --> xfs
/var - 6gb --> xfs
/tmp 2gb --> xfs
/home - 1.5gb --> xfs
/ - 15gb --> xfs
/var/lib/docker - 10gb --> ext4
Bloquear acesso SSH para root e configurar o SSH:

Editar o arquivo sshd_config
Descomentar a linha PermitRootLogin e deixa-lo com valor: no
Configurando o redirecionamento de portas:![179813903-be572f3f-b1b6-4644-9db4-ad5a13a744ae](https://user-images.githubusercontent.com/109623573/179865405-82a69b32-07e5-42d9-b86f-e1699ea55807.png)
Ajustar DNS:
Editar o arquivo hosts do Windows e do Linux, adicionando a linha: 127.0.0.1 elklabmonitoriacontainer
Ajustar rede:
Modo NAT nas configurações de rede da VM:
