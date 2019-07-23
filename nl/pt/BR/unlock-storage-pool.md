---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: unlock storage pool, set up device

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

# Desbloqueando o conjunto de armazenamentos
{: #unlock-storage-pool}

É possível copiar dados para o dispositivo {{site.data.keyword.mdms_full}} primeiro desbloqueando e ativando o conjunto de armazenamentos provisionado para o dispositivo.
{: shortdesc}

## Recuperando a passphrase de seu conjunto de armazenamentos (beta)
{: #retrieve-storage-pool-passcode}

Para acessar o conjunto de armazenamentos no dispositivo {{site.data.keyword.mdms_short}}, recupere as credenciais de seu dispositivo navegando até os detalhes da solicitação do {{site.data.keyword.mdms_short}} no console do {{site.data.keyword.cloud_notm}}.

Esse recurso está disponível como parte da [liberação beta do {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). Também é possível acessar credenciais para seu dispositivo de armazenamento na seção _Detalhes da solicitação_ do [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Para recuperar a passphrase de seu conjunto de armazenamentos:

1. [Faça login no console do {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Acesse **Menu** &gt; **Lista de recursos** para visualizar uma lista de seus recursos.
3. Em sua lista de recursos do {{site.data.keyword.cloud_notm}}, selecione a sua instância provisionada do {{site.data.keyword.mdms_short}}.
4. Na guia _Detalhes da solicitação_, navegue até a seção Credenciais.
5. Copie o valor de **Senha de bloqueio do conjunto**.

## Ativando o conjunto de armazenamentos
{: #activate-storage-pool}

Desbloqueie o conjunto de armazenamentos vazio usando as credenciais recuperadas na etapa anterior.

1. [Efetue login na interface com o usuário do dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-access-ui#log-in-ui).
2. No assistente Tarefas comuns, clique em **Desbloquear e iniciar o conjunto de armazenamentos**.
3. Insira a passphrase do conjunto de armazenamentos recuperada na etapa 1 e clique em **OK**.
      
   ![Ativar o conjunto de armazenamentos](/images/StartStoragePool.png)

   Por padrão, o compartilhamento tem os protocolos Network File System (NFS) e Bloco de Mensagens do Servidor (SMB) ativados sem restrições de acesso. É possível modificar o acesso a esse compartilhamento para NFS ou SMB clicando com o botão direito no nome do compartilhamento na interface com o usuário e, em seguida, selecionando a opção de menu apropriada.
   {: note}

## Etapas Seguintes
{: #unlock-storage-pool-next-steps}

- Se estiver usando uma máquina Unix, [conecte o compartilhamento de rede usando o NFS](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-nfs-share).
- Se estiver usando uma máquina Windows, [conecte o compartilhamento de rede usando o SMB](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-connect-smb-share).
- Inicie o [processo de cópia de dados](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-data-copy).
