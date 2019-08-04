# Samba 4
Samba é um programa de computador, utilizado em sistemas operacionais do tipo Unix, que simula um servidor Windows, permitindo que seja feito gerenciamento e compartilhamento de arquivos em uma rede Microsoft.

## Instalação
Toda a instalação é feita como **root**

### Debian

Configuração do hostmane, edite o arquivo:

`/etc/hostname`
Alterando o nome para nome.dominio.local

Salve e feche o editor

Onde: O **nome** é o nome da máquina, **dominio** é o nome para o Controlador de Domínio.

Instale o pacote do samba4 com o comando:
`apt-get install samba`

Instale o pacote do Kerberous com o comando
`apt-get install krb5-config`

Instale o pacote do Winbind com o comando
`apt-get install winbind`

Instale o pacote do samba client com o comando:
`apt-get install smbclient`




### CentOS

Instalação por código fonte

Baixe o pacote do samba no site [http://www.samba.org/samba/ftp/stable](http://www.samba.org/samba/ftp/stable), lembrando que estamos Instalando a versão 4.

**Obs**: Para esta documentação baixei a versão 4.10.6 com o comando:

`wget https://download.samba.org/pub/samba/stable/samba-4.10.6.tar.gz`

Entre na pasta samba-4.10.6 recém criada, execute o comando:

`cd samba-4.10.6`

Obs: Basta alterar o nome da pasta para outras versões.

Inicie o processo de compilação do Samba 4, como root execute o comando:

`./configure --enable-debug --enable-selftest`

Compile e instale o Samba 4, como root execute o comando:

`make && make install`
Crie alguns links simbólicos, como root execute os comandos:

```
ln -s /usr/local/samba/sbin/samba /bin/samba
ln -s /usr/local/samba/bin/smbclient/bin/smbclient
```

Inicie a instalação do Active Directory, como root execute o comando:

## Colocando Estações no Domínio

Coloque a/as estação/ões Windows no domínio siga os passos clicando aqui

## Criando Políticas de Segurança (GPO)

Para criar política/s de segurança (GPO) siga os passos clicando aqui

## Comandos Samba 4

Para listar os usuários ou trocar a senha clique aqui