---
copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}


# Montando um ISO em um servidor bare metal

## Visão geral

Embora a maioria dos clientes {{site.data.keyword.Bluemix_notm}} use um dos Sistemas Operacionais padrão que vêm com os nossos servidores, é possível montar os ISOs customizados (imagens do disco) em servidores. Há três opções para montar os ISOs customizados.

Para que os métodos funcionem, é necessário estar conectado à rede privada por meio do serviço VPN SL, como o
[SoftLayer SSL VPN Portal - AMS01](https://vpn.ams01.softlayer.com/prx/000/http/localhost/login) ou por meio de outro servidor já conectado à rede.

**Nota:** as imagens do disco de hardware Lenovo maiores que 50 MB devem ser montadas usando a guia Interface do console do IMM > mídia.

## Opção 1 (preferencial): usando IPMI (ISO em um compartilhamento CIFS)

Se você já tiver a infraestrutura implementada no {{site.data.keyword.Bluemix_notm}}, será possível configurar um servidor existente para oferecer um compartilhamento CIFS para a rede interna. Será possível então montar qualquer ISO em um servidor bare metal.

Esse é o método preferencial para instalar um S.O. customizado em um Bare Metal Server porque ele é instalado sobre a rede
local, que é muito rápida e pode manter um ISO montado mesmo se você efetuar logout ou for desconectado da interface de
gerenciamento.

Siga estas etapas para instalar um S.O. customizado por meio de um compartilhamento CIFS:

1. Certifique-se de que tenha colocado o ISO no compartilhamento CIFS.
* Efetue login no console de gerenciamento do IPMI apontando o navegador da web para o IP especificado em
https://control.softlayer.com/ e em dispositivos -> seu servidor (detalhes do dispositivo) -> Gerenciamento remoto. O nome do usuário e a senha também são especificados aqui.
* Passe o mouse sobre a **Mídia virtual** e clique em **Imagem de CD-ROM**
* Preencha os detalhes apropriados, clique em **Salvar e montar**.
* Nem todos os usuários têm permissão para mudar o BIOS do servidor. Se necessário, é possível abrir um chamado para o suporte solicitando:
  * privilégios de administrador de usuário raiz no IPMI (para poder mudar o modo de Conexão de mídia virtual)
  * Mude a sequência de inicialização para ‘Disco virtual do IPMI’ como primeira opção de inicialização.
* Depois que essas mudanças tiverem sido feitas, volte para o console de gerenciamento do IPMI e acesse configuração -> Sessão remota e mude o modo de conexão para **conectar**. Em alguns consoles do IPMI mais antigos, é possível ignorar essa opção.
* Reinicialize o servidor e inicialize por meio da mídia virtual.


## Opção 2: usando o IPMIView (ISO em um compartilhamento CIFS)

Pré-requisitos:<br/>
* Você tem um ISO inicializável
* Um Windows CIFS Server ou Armazenamento NAS para armazenar o ISO inicializável
* O ISO é transferido por upload para o File Storage (NAS) associado ao servidor.
* O IPMIView está instalado ou acesso ao Console KVM <!--  * http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* http://knowledgelayer.softlayer.com/procedure/access-kvm-console -->
* O arquivo ISO é transferível por download usando wget
* Você tem acesso SSH com privilégios para acessar/instalar pacotes e criar uma montagem


### Linux e Windows
Siga as etapas abaixo para montar um ISO com IPMIView.
1. Por meio de um chamado de suporte, solicite que o servidor inicialize o CD-ROM Virtual como o primeiro dispositivo. Cada dispositivo deve inicializar por meio de seu CD-ROM virtual associado. É possível reverter essa configuração após a instalação do S.O.
* Estabeleça uma Conexão VPN para [VPN](http://www.softlayer.com/VPN-Access). Se você estiver usando o Microsoft Internet Explorer, certifique-se de incluir .softlayer.com em sua lista de Sites confiáveis e mantenha seu JAVA atualizado.
* Copie a Mídia ISO para o NAS ou Windows CIFS Server.
  * Conecte-se ao seu Linux jumpbox usando SSH.
  * Monte o compartilhamento NAS em seu Linux jumpbox:

        mkdir /mnt/nasmount
        mount -t cifs //NAS_SERVER_NAME_ORIP/SLN#####-2 -o username=SLN#####-2,
        password=NAS_STORAGE_PW,rw,nounix,iocharset=utf8,file_mode=0644,dir_mode=0755 /mnt/nasmount
  * Monte a chave de parâmetro de Comando:
        NAS_SERVER_NAME_ORIP = o nome ou IP do armazenamento NAS.
        /SLN#####-2 = o nome do usuário e o nome da pasta para se conectar a seu armazenamento NAS.
        NAS_STORAGE_PW = a senha para seu armazenamento NAS.
        /mnt/nasmount = a Pasta para montar o armazenamento NAS.
  * Mude o diretório para sua nova pasta de montagem do NAS.
        cd /mnt/nasmount
  * Faça download do arquivo iso usando wget.
        wget http://www.linktoyouriso.com/isofilename.iso
  Você verá uma confirmação de que o download foi bem-sucedido.
* Faça download da Visualização do IPMI aqui:
      http://knowledgelayer.softlayer.com/procedure/download-ipmiview
* Conecte-se ao Servidor sobre o IP de Gerenciamento.
      http://knowledgelayer.softlayer.com/procedure/log-ipmiview
      http://knowledgelayer.softlayer.com/procedure/view-ipmi-credentials
* Abra a guia de Mídia virtual
* Conclua os detalhes da conexão da imagem de CD-ROM.
  *
    * Host de compartilhamento = o Endereço IP do Armazenamento NAS. É possível localizar esse valor efetuando ping do nome do servidor de armazenamento NAS. Por exemplo,  _ ping nas501.service.softlayer.com _
    * Nome de compartilhamento = o Nome do usuário do armazenamento NAS
    * Caminho para a imagem = o nome do arquivo ISO, no formato a seguir:
          \NASusername\isoname.iso (ou seja, \SLN123456\centos6.iso)
    * Usuário = o nome do usuário do armazenamento NAS
    * Senha = a Senha para o armazenamento NAS
* Reinicialize o servidor
* Abra a visualização Console KVM
* Siga os prompts do sistema para Inicializar o ISO INICIALIZÁVEL
* Instale o S.O.>
* Desmonte a Mídia virtual
* Reinicie o Servidor

## Opção 3: montando um ISO de seu computador local
<a name="option3"></a>

É possível montar um ISO de seu computador local usando o visualizador iKVM Java (console). Isso permitirá montar um ISO enquanto conectado ao console. A velocidade de progresso da instalação pode variar dependendo da velocidade de upload e latência de sua conexão de Internet, desempenho do Java e seu computador.

Se você não tem permissão para mudar o BIOS em um servidor, abra um chamado de suporte solicitando as mudanças a seguir:
* Privilégios de administrador de usuário raiz no IPMI (para poder mudar o modo de Conexão de mídia virtual)
* Para mudar a sequência de inicialização para ‘Disco virtual do IPMI’ como primeira opção de inicialização. (Como o ISO ainda não está montado, o suporte deverá mudar somente a prioridade do dispositivo de inicialização por enquanto).


1. Efetue login no console de gerenciamento do IPMI apontando o navegador da web para o IP especificado em
https://control.softlayer.com/.
* Clique em Dispositivos > seu servidor (detalhes do dispositivo) > Gerenciamento remoto. Especifique o nome do usuário e a senha.
* Clique em Configuração > Sessão remota e mude o modo de conexão para **conectar**. Em alguns consoles do IPMI mais antigos, essa opção não está disponível, portanto é possível ignorar esta etapa.
* Clique em Sistema > Informações do sistema para retornar à página de informações do sistema. Você verá um ícone de janela do console.
* Clique no ícone do console para abrir o console. Aceite todos os avisos de segurança.
* Quando o console estiver conectado, você verá o prompt de login.
* Clique em Mídia virtual > Armazenamento virtual
* Acesse a guia **CD-ROM&TWBAMP e ISO** e selecione o Arquivo ISO em **Tipo de unidade lógica**
* Clique em **Abrir imagem** e selecione o ISO em seu computador local
* Clique em **Plug-in** para inserir o ISO na unidade de CD-ROM virtual.
* Clique em **OK**.
* Reinicialize o servidor e use a opção **inicializar por meio da unidade de CD-ROM virtual**. Você pode precisar usar o teclado virtual no visualizador do iKVM para selecionar um dispositivo de inicialização.

## Resolução de problema

* Nem todos os usuários têm acesso padrão para montar a Mídia virtual. Se um erro de permissão ocorrer, entre em contato com o Suporte para uma atualização para as permissões de Usuário raiz do IPMI.
* Se um ISO já estiver montado, uma mensagem de erro aparecerá com o texto **Há um disco montado**. Deve-se desmontar o disco existente e substituí-lo pelo novo ISO. Dois ISO não podem estar montados ao mesmo tempo.
* Você pode precisar entrar em contato com o suporte para mudar a ordem de inicialização no BIOS.
* Ao montar um ISO, use a VPN SSL (http://vpn.softlayer.com) em vez de VPN PPTP.  Depois de conectado à rede VPN, também é possível acessar o IPMI do sistema por meio do endereço do IPMI (https://<private-ip-IPMI-management>).
* Ao inserir um caminho para um ISO, use a sintaxe de nome UNC (Convenção Universal de Nomenclatura) para o caminho, por
exemplo: _\\<nome do usuário do NAS>\<isoname>.iso _
