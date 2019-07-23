---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: return device, ship device, disconnect device, shipping label

subcollection: mass-data-migration

---
{:new_window: target="_blank"}
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

# Retornando o dispositivo
{: #return-device}

Desligue e retorne seu dispositivo {{site.data.keyword.mdms_full}} para o {{site.data.keyword.cloud_notm}} para concluir o processo de migração.
{: shortdesc}

## Desconectando o dispositivo
{: #disconnect-device}

Quando o processo de cópia de dados for concluído, será possível desligar o sistema normalmente.

1. No assistente Tarefas comuns, clique em **Encerrar dispositivo**.

    ![Encerrando o dispositivo](images/ShutDown.png)

    Clique em  ** OK **  para confirmar.
2. Desligue o dispositivo usando seu botão **Sistema ligado/desligado**. 
3. Configure o **Comutador principal** como **Desligado**.
4. Enrole e retorne todos os cabos e lentes para seus locais de armazenamento dentro do estojo de transporte.

## Enviando o dispositivo para o {{site.data.keyword.cloud_notm}}
{: #ship-device}

Prepare seu rótulo de envio e notifique sua transportadora quando estiver pronto para devolver o dispositivo.

1. Recupere a lista de inventário e o rótulo de envio de devolução para o dispositivo. Estes documentos estão localizados sob a tampa do estojo de transporte.

    Se estiver enviando diversos dispositivos, lembre-se de que o rótulo do envio de devolução fornecido em cada caso é específico do dispositivo de armazenamento. Antes de agendar uma coleta com a transportadora, verifique se o rótulo de envio de devolução correspondente está afixado no dispositivo apropriado.
    {: note}
2. Use a lista de inventário para verificar se todos os cabos e lentes foram retornados e armazenados no estojo de transporte.
3. Retorne a lista de inventário ao caso de transporte e, em seguida, use as instruções listadas no rótulo de envio de devolução para afixar o rótulo ao dispositivo.
4. Agende uma coleta com sua transportadora e devolva o dispositivo ao data center.

    Quando o dispositivo é retornado para o {{site.data.keyword.cloud_notm}}, o status do pedido muda para _Dispositivo recebido_ na página de detalhes da solicitação do {{site.data.keyword.mdms_short}}.

## Etapas Seguintes
{: #return-device-next-steps}

- Verifique o status de seu pedido [gerenciando sua solicitação do {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Antes de excluir dados do seu servidor de origem, [verifique se eles foram transferidos por upload com sucesso para o {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-verify-data).

