---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: get started tutorial, data transfer, data migration, transfer data to cloud, migrate data, migrate data to cloud, Mass Data Migration

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

# Tutorial Introdução
{: #getting-started-tutorial}

O {{site.data.keyword.mdms_full}} ajuda você a mover terabytes ou petabytes de dados para o {{site.data.keyword.cloud_notm}} de maneira rápida, simples e segura. Este tutorial mostra como solicitar seu dispositivo de migração usando o {{site.data.keyword.slportal}}.
{: shortdesc}

Interessado em experimentar novos recursos do {{site.data.keyword.mdms_short}}? É possível visualizar aprimoramentos de serviços futuros participando do programa beta do {{site.data.keyword.mdms_short}}. Para obter mais informações, consulte [Obtendo acesso ao beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: tip}

## Antes de iniciar
{: #get-started-prereqs}

Antes de solicitar um dispositivo {{site.data.keyword.mdms_short}}:

- Planeje sua migração revisando as [regiões e locais](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-regions) nos quais o {{site.data.keyword.mdms_short}} está disponível.
- Certifique-se de ter uma instância provisionada do [{{site.data.keyword.cos_full}}](https://{DomainName}/catalog/services/cloud-object-storage){: external} para sua conta do {{site.data.keyword.cloud_notm}}. 
- Compreenda os tipos e velocidades de sua conexão de rede.
- Reúna suas configurações de rede, como endereços IP e outros detalhes de roteamento, para conectar o dispositivo ao seu servidor de origem.
- Identifique uma pessoa que possa receber, conectar e usar o dispositivo em seu local.

## Criando um depósito de armazenamento
{: #get-started-create-bucket}

Depois de provisionar uma instância do Cloud Object Storage, crie um depósito de armazenamento para configurar um destino para seus dados migrados. 

1. Na lista de recursos do {{site.data.keyword.cloud_notm}}, selecione sua instância provisionada do Cloud Object Storage.
2. Na página _Introdução_, clique em **Criar depósito**.
3. Insira um nome de depósito e selecione uma opção de resiliência para seus dados.
   
   A opção de resiliência determina como seus dados são distribuídos pelo serviço Cloud Object Storage em uma área geográfica depois de serem importados para o serviço. O {{site.data.keyword.mdms_short}} suporta todas as opções de resiliência disponíveis para o Cloud Object Storage.  
   {: note}
4. Na lista de locais, selecione a área geográfica na qual deseja que seus dados sejam fisicamente armazenados após sua migração para o depósito de armazenamento.
5. Na lista de classes de armazenamento, selecione **Padrão**.
6. Clique em **Criar depósito**.

## Solicitando um dispositivo
{: #get-started-request-device}

É possível solicitar um dispositivo {{site.data.keyword.mdms_short}} usando o {{site.data.keyword.slportal}}.

1. Efetue login no [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external}.
2. No menu de navegação, clique em **Armazenamento** > **Migração de dados** > **{{site.data.keyword.mdms_short}}** para acessar a página inicial do {{site.data.keyword.mdms_short}}.
3. Clique em **Solicitar dispositivo** para abrir o formulário do pedido.
4. Comece sua solicitação do {{site.data.keyword.mdms_short}} especificando os detalhes a seguir.

    <table>
      <tr>
        <th>Ações</th>
        <th>Descrição</th>
      </tr>
      <tr>
        <td>Incluir um nome para a solicitação</td>
        <td>Insira um alias para identificar e rastrear sua solicitação do {{site.data.keyword.mdms_short}}.</td>
      </tr>
      <tr>
        <td>Selecionar o destino da transferência de seus dados</td>
        <td>Na lista suspensa, selecione sua instância provisionada do Cloud Object Storage. Em seguida, selecione o nome designado ao depósito de armazenamento no qual deseja armazenar seus dados migrados.</td>
      </tr>
      <tr>
        <td>Incluir um endereço de entrega</td>
        <td>Insira suas informações de envio, como o endereço de entrega e o nome da pessoa que aceitará a entrega.</td>
      </tr>
      <tr>
        <td>Incluir contatos de migração</td>
        <td>Insira o nome da pessoa que gerenciará a migração de dados para seu dispositivo.</td>
      </tr>
      <tr>
        <td>Definir configurações de rede</td>
        <td>
          <p>Defina configurações para a conexão de transferência de dados inserindo seus detalhes de configuração de rede.</p>
          <p>Forneça as seguintes <a href="/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview#network-settings">configurações de rede</a>:</p>
          <p>
            <ul>
              <li><i>Configurações de gerenciamento de dispositivo.</i> Insira o endereço IP estático, a máscara de rede e o gateway padrão do seu computador remoto.</li>
              <li><i>Configurações de transferência de dados.</i> Insira o endereço IP estático e a máscara de rede do servidor no qual seus dados de origem estão.</li>
            </ul>
          </p>
        </td>
      </tr>
      <caption style="caption-side:bottom;">Tabela 1. Descreve o fluxo de trabalho de solicitação do {{site.data.keyword.mdms_short}}</caption>
    </table>

    Ao selecionar um local de entrega para seu dispositivo, considere o peso do dispositivo e a acessibilidade. O dispositivo, com seu estojo rígido e um estojo de viagem de espuma, pesa cerca de 60 libras. Para ajudar no transporte do dispositivo, o estojo de viagem é equipado com rodas e uma alça pop-up para facilitar manobras.
    {: tip}
5. Leia o contrato de prestação de serviços do {{site.data.keyword.mdms_short}} e, em seguida, selecione a caixa de seleção.
6. Clique em **Realizar solicitação** para concluir seu pedido. 

## O que vem a seguir
{: #get-started-next-steps}

Sucesso! Está tudo pronto com sua solicitação do {{site.data.keyword.mdms_short}}.

- Para saber mais sobre como rastrear seu pedido, consulte [Gerenciando sua solicitação](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-request).
- Para saber mais sobre como receber e conectar seu dispositivo, consulte [Configurando o dispositivo](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-device-overview).

