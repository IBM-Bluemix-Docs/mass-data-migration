---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: copy data to device, move data to device, 

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

# Copiando dados para o dispositivo
{: #copy-data}

É possível copiar dados para um dispositivo {{site.data.keyword.mdms_full}} usando a interface com o usuário do dispositivo.

## Copiando dados para o dispositivo
{: #copy-data}

Depois de conectar seu servidor ao compartilhamento de rede, será possível iniciar e monitorar a cópia de dados no dispositivo.

1. Copie os dados para o compartilhamento de rede usando uma ferramenta de cópia de arquivos compatível com seu computador host.
2. No assistente Tarefas comuns, clique em **Visualizar atividade de rede** para mostrar o carregamento de Ethernet de entrada, à medida que os dados são transferidos para o dispositivo no link de 10Gb.
   
    ![Visualizar atividade](images/NetworkPerf.png)
3. Clique em **Visualizar o conjunto de armazenamentos** para monitorar o uso de armazenamento e o IOPS no dispositivo.
   
    ![Visualizar o conjunto de armazenamentos](images/PoolPerf.png)

## Etapas Seguintes
{: #import-data-next-steps}

- [Desligue normalmente o dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-disconnect-device).
- Prepare o rótulo de envio e [retorne o dispositivo para o {{site.data.keyword.cloud_notm}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-ship-device).
