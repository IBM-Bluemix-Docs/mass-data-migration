---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

# Gerenciando sua solicitação
{: #manage-request}

Gerencie e rastreie o status de seu pedido do {{site.data.keyword.mdms_full}} usando o {{site.data.keyword.slportal}}.
{: shortdesc}

Ao participar do programa beta do {{site.data.keyword.mdms_short}}, é possível visualizar um novo painel de serviço do {{site.data.keyword.mdms_short}}, que pode ser acessado por meio do console do {{site.data.keyword.cloud_notm}}. Para obter mais informações, consulte [Obtendo acesso ao beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Rastreando seu pedido 
{: #track-order}

Após solicitar um dispositivo de armazenamento, é possível rastrear o progresso do seu pedido usando a [página de detalhes da solicitação do {{site.data.keyword.mdms_short}}](https://control.softlayer.com/storage/mdms){: external} disponível no {{site.data.keyword.slportal}}.

A tabela a seguir mostra como o status do pedido é mudado conforme o {{site.data.keyword.mdms_short}} processa a solicitação.

| Status | Descrição |
| --- | --- |
| Processando a solicitação | Depois que o {{site.data.keyword.mdms_short}} recebe a solicitação, o status é mudado para _Processando solicitação_. |
| Preparando o dispositivo | Após a aprovação de seu pedido, o status da solicitação é mudado para _Preparando o dispositivo_. O {{site.data.keyword.mdms_short}} prepara e configura o próximo dispositivo de armazenamento disponível.  |
| Aguardando envio | O dispositivo de armazenamento pré-configurado está aguardando o envio para o seu local. Após a solicitação entrar no status _Aguardando envio_, o pedido não poderá mais ser cancelado. |
| Dispositivo enviado | O dispositivo de armazenamento é coletado pela transportadora e enviado para o seu local. É possível visualizar o número de rastreamento na seção _Detalhes do pedido_ da [página de detalhes da solicitação](https://control.softlayer.com/storage/mdms){: external}. |
| Dispositivo recebido | Depois que o dispositivo é retornado para o {{site.data.keyword.cloud_notm}}, o status muda para _Dispositivo recebido_. |
| Transferindo dados | Durante o processo de transferência de dados, o status da solicitação é mudado para _Transferindo dados_. O dispositivo é conectado à rede no data center do {{site.data.keyword.cloud_notm}} e a transferência de dados começa automaticamente.  |
| Transferência concluída| Quando o processo de transferência estiver concluído, o status da solicitação mudará para _Transferência concluída_. Seus dados agora estarão disponíveis no destino do Cloud Object Storage especificado na solicitação inicial. |
| Limpeza concluída | O {{site.data.keyword.mdms_short}} apaga permanentemente os dados do dispositivo usando os padrões de limpeza de dados NIST. Depois que o processo de limpeza de dados for concluído, o status do pedido mudará para _Limpeza concluída_.
{: caption="Tabela 1. Descreve o fluxo de trabalho do status do pedido do {{site.data.keyword.mdms_short}}" caption-side="top"}
