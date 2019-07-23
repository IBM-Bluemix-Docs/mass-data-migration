---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: mount SMB share, SMB, Active Directory, AD, access network share, connect to network share

subcollection: mass-data-migration

---

{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Conectando-se ao compartilhamento de rede usando o SMB
{: #connect-smb-share}

Para se preparar para a cópia dos dados, é possível acessar o compartilhamento de rede no dispositivo {{site.data.keyword.mdms_full}} usando o protocolo Bloco de Mensagens do Servidor (SMB).
{: shortdesc}

Antes de se conectar ao compartilhamento:

- Determine se é necessário associar o dispositivo {{site.data.keyword.mdms_short}} ao Active Directory. Se você estiver montando o compartilhamento de rede em um servidor Windows associado ao Active Directory, também deverá [associar o dispositivo ao domínio do Active Directory](#use-active-directory) antes de ser possível se conectar ao compartilhamento.
- Determine se seu ambiente requer a assinatura do SMB. A associação do dispositivo {{site.data.keyword.mdms_short}} ao Active Directory permite a assinatura do SMB por padrão. Se seu ambiente não precisar da assinatura do SMB, será possível [desativar a assinatura do SMB no cliente](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share) para evitar problemas de conexão e aumentar o desempenho de sua transferência de dados.

## Gerenciando o acesso ao compartilhamento do SMB
{: #manage-smb-share-access}

Por padrão, o compartilhamento de rede está configurado para ter acesso público. Antes de montar o compartilhamento em seu servidor, é possível incluir nele regras de acesso do SMB para corresponder aos seus requisitos de ambiente ou segurança. 

Para obter informações detalhadas sobre como controlar o acesso a compartilhamentos no dispositivo de armazenamento, consulte a [documentação do OSNEXUS QuantaStor](https://wiki.osnexus.com/index.php?title=Network_Shares){:external}.
{: tip}

Para modificar o acesso ao compartilhamento do SMB:

1. [Efetue login na interface com o usuário do dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. No assistente Tarefas comuns, clique em **Visualizar compartilhamentos de rede** para exibir a visualização dos compartilhamentos de rede.

   ![Ícones do fluxo de trabalho](images/workflow.png)
3. Feche o assistente Tarefas comuns e, em seguida, clique com o botão direito no nome do compartilhamento de rede para visualizar uma lista de opções. 
4. Clique em **Modificar o acesso ao compartilhamento e ao SMB** para modificar o acesso ao compartilhamento do SMB.

    ![Modificar o acesso ao compartilhamento do SMB](images/add-smb-access.png)

## Usando o Active Directory
{: #use-active-directory}

Se estiver usando o SMB em um servidor Windows, será possível gerenciar as permissões de acesso, a propriedade de arquivo e os atributos de arquivo dos seus dados associando o dispositivo {{site.data.keyword.mdms_short}} ao Active Directory. A associação do dispositivo a um domínio do Active Directory permite o acesso do SMB para usuários específicos e grupos do AD. 

Para saber mais sobre como associar o dispositivo ao Active Directory, consulte a [documentação do OSNEXUS QuantaStor](https://wiki.osnexus.com/index.php?title=Network_Shares#Joining_an_AD_Domain){:external}.

## Montando o compartilhamento do SMB em um sistema Windows
{: #mount-smb-share}

Depois de desbloquear e ativar o conjunto de armazenamentos no dispositivo, conecte-se ao compartilhamento do SMB usando a caixa de diálogo **Mapear a unidade de rede** em seu computador Windows.

Para montar o compartilhamento de rede:

1. [Efetue login na interface com o usuário do dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. No assistente Tarefas comuns, clique em **Visualizar compartilhamentos de rede** para exibir a visualização dos compartilhamentos de rede.
3. Feche o assistente Tarefas comuns e, em seguida, clique com o botão direito no nome do compartilhamento de rede para visualizar uma lista de opções. 
4. Clique em **Visualizar comando de montagem** para revisar as informações de montagem do compartilhamento.
5. Faça ping do endereço IP listado na caixa de diálogo para testar a conectividade de rede entre o seu computador e o dispositivo {{site.data.keyword.mdms_short}}.

   Certifique-se de que o endereço IP corresponda à [porta de transferência de dados de 10 GbE](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings) no dispositivo.
   {: note} 
6. No Explorador de arquivos, clique com o botão direito em **Rede** e, em seguida, selecione **Mapear unidade de rede** para abrir a caixa de diálogo Mapear unidade de rede.

   ![Abrir a caixa de diálogo Mapear unidade de rede](images/map-network-drive.png)
7. Insira o endereço IP testado na etapa 1 e clique em **Procurar**.

   ![Conectar-se ao compartilhamento de rede](images/map-network-drive-dialog.png)
8. Na lista de pastas de rede, selecione o compartilhamento do {{site.data.keyword.mdms_short}}. Clique em  ** OK **  para confirmar.
9. Clique em **Concluir** para montar o compartilhamento no seu servidor de origem.

    Caso seja possível fazer ping do endereço IP, mas não for possível montar o compartilhamento, é provável que a assinatura do SMB esteja ativada para o cliente Windows. Considere [desativar a assinatura do SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-troubleshooting#unable-to-mount-smb-share) no cliente e tente novamente.
    {: tip} 

## Etapas Seguintes
{: #connect-smb-share-next-steps}

- Inicie o [processo de cópia de dados](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-copy-data).
