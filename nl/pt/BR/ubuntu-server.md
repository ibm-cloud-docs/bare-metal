---
copyright:
  years: 1994, 2017
lastupdated: "2017-12-14"
---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Instalando o servidor Ubuntu em um servidor bare metal

Se você deseja usar um sistema operacional que não é fornecido pelo {{site.data.keyword.IBM&reg; Cloud}}, é possível instalá-los em servidores bare metal montando os ISOs customizados (imagens de disco). Para montar um ISO, faça upload dele no Armazenamento de arquivos (NAS) associado ao servidor. Para fazer upload de um ISO para NAS, use os procedimentos a seguir para montar um ISO com IPMI.
1. Peça o Servidor Bare Metal **Sem sistema operacional** 
* Também é possível selecionar o S.O. livre (por exemplo, CentOS) como o sistema operacional que pode ser usado para se conectar ao NAS.
* Peça ao armazenamento NAS para armazenar o ISO inicializável. Se você já tiver qualquer servidor Windows CIFS, será possível usá-lo para compartilhar a imagem ISO. Com esse servidor Windows CIFS, você obterá o NAS anterior com capacidade de 20 GB. Após o fornecimento do NAS, é possível ver a descrição de seu NAS no portal do cliente.
* Faça download da imagem ISO em https://www.ubuntu.com/download/server.
* Faça upload da imagem ISO para NAS ou Windows CIFS Server. Se você tiver o armazenamento NAS, será possível fazer upload do arquivo de imagem ISO usando FTP.

  Procedimento de FTP de amostra:
  ```
  #ftp <nas address>.service.softlayer.com
  Connected to <nas address>.service.softlayer.com
  220 NAS FTP Service
  User (<nas address>.service.softlayer.com:(none)): <nas username>
  331 Please specify the password.
  Password: <nas password>
  230 Login successful.
  ftp> bin
  200 Switching to Binary mode
  ftp> put <iso imagefile name>.iso
  200 PORT command successful. Consider using PASV.
  150 Ok to send data.
  226 Transfer complete.
  ftp: 3170893824 bytes sent in 253.86 Seconds 12490.77Kbytes/sec.
  ```
  
* Estabeleça uma Conexão VPN para o {{site.data.keyword.Bluemix_notm}} com o IPMI. É possível ativar o menu VPN no menu Suporte ou na URL a seguir: [Acesso à VPN](http://www.softlayer.com/VPN-Access)
* Monte a imagem ISO no Menu de Mídia Virtual do IPMI usando Conectar-se ao IPMI sobre o IP de gerenciamento.
  1. Visualize as credenciais do IPMI
  * Registre a visualização IPMI
  * Abra a guia de Mídia virtual
  * É necessário o usuário raiz com privilégios de Administrador no IPMI. Se os privilégios forem mostrados como *Operador*, abra um chamado de suporte para mudar os privilégios para Administrador.
  * Preencha os detalhes da conexão da imagem ISO
    Host de compartilhamento = o endereço IP do NAS<br/Exemplo: 10.3.x.x
    Caminho para a imagem = o nome do arquivo ISO, formatado como este: \NASusername\imagefilesname.iso (ou seja, \SLNxxxxxx\SLE-12-SP1-Server-DVD-x86_64-GM-DVD1.iso)
    Usuário = o nome do usuário do NAS
    Senha = a senha para o NAS
  * Clique no botão **Montar**
  * Confirme o dispositivo
* Clique e ative o Visualizador KVM e abra a página Armazenamento virtual no menu Mídia virtual. Se a montagem de sua imagem ISO como dispositivo de CD-ROM for bem-sucedida, você verá a descrição do dispositivo no **Histórico de status da conexão**.
* Solicite que seu servidor inicialize o CD-ROM Virtual como o primeiro dispositivo por meio do chamado do SoftLayer. Conclua esta solicitação para cada servidor. Você muda a configuração de inicialização após o S.O. ser instalado.
  **Nota**: você talvez não precise entrar em contato com o suporte para mudar a ordem de inicialização no BIOS. Isso depende do seu servidor. Tente reinicializar uma vez para confirmar a ordem de inicialização.
* Reinicialize o servidor por meio da visualização KVM.
* Instalar o S.O. da imagem ISO montada.
* Instale o S.O. Ubuntu no servidor bare metal por meio do ISO.
* Defina as configurações de rede (endereço IP/sub-rede/gateway/DNS etc.). Se você não configurar isso corretamente durante a etapa de instalação, só será possível se conectar a esse servidor por meio do console KVM após a reinicialização.

* Desmonte a mídia virtual. É necessário desmontar a mídia virtual do servidor por meio da guia Mídia Virtual do IPMI.
* Reinicialize o servidor.
* Após a reinicialização, é possível acessar o servidor por meio de SSH.
