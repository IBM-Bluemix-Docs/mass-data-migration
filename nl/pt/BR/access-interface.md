---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: device user interface, access device, log in to device

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

# Acessando a interface com o usuário do dispositivo
{: #access-ui}

Depois de configurar o dispositivo {{site.data.keyword.mdms_full}} para a conectividade Ethernet, você estará pronto para acessar a interface com o usuário do dispositivo para que seja possível interagir com ele e começar o processo de migração de dados.
{: shortdesc}

## Recuperando as credenciais do seu dispositivo (beta)
{: #retrieve-device-credentials}

Quando você envia uma solicitação do {{site.data.keyword.mdms_short}}, o serviço gera automaticamente credenciais em seu nome que podem ser usadas para acessar a IU da web local para o dispositivo. 

Esse recurso está disponível como parte da [liberação beta do {{site.data.keyword.mdms_short}}](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta). Também é possível acessar credenciais para seu dispositivo de armazenamento na seção _Detalhes da solicitação_ do [{{site.data.keyword.slportal}}](https://control.softlayer.com/storage/mdms){: external}.
{: note}

Para recuperar as credenciais de seu dispositivo:

1. [Faça login no console do {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Acesse **Menu** &gt; **Lista de recursos** para visualizar uma lista de seus recursos.
3. Em sua lista de recursos do {{site.data.keyword.cloud_notm}}, selecione a sua instância provisionada do {{site.data.keyword.mdms_short}}.
4. Na guia _Detalhes da solicitação_, navegue até a seção Credenciais.
5. Copie os valores de **Nome de usuário** e **Senha**.

## Efetuando login na interface com o usuário do dispositivo
{: #log-in-ui}

Use as credenciais do dispositivo recuperadas na etapa anterior para efetuar login na IU da web local e interagir com o dispositivo {{site.data.keyword.mdms_short}}.

1. Abra um navegador da web e navegue até o endereço IP estático fornecido no formulário de pedido.

   ```
   https://<device_management_IP_address>
   ```
   {: codeblock}

   Substitua `<device_management_IP_address>` pelo endereço IP configurado para suas portas de rede Eth1 ou Eth2. Aceite a exceção de certificado.

2. Faça login na IU do dispositivo usando o nome de usuário e a senha recuperados na etapa anterior. 

   ![Página de login](images/login.png)
   
   O assistente Tarefas comuns é exibido. Use as opções da esquerda para a direita para começar a importar seus dados.

   ![Ícones do fluxo de trabalho](images/workflow.png)

   É possível reabrir o assistente Tarefas comuns usando o **Gerenciador de fluxo de trabalho** na área superior esquerda da interface.
   {:tip}

## Etapas Seguintes
{: #access-ui-next-steps}

- Para preparar-se para a cópia de ingestão de dados, comece [desbloqueando o conjunto de armazenamentos no dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-unlock-storage-pool).
