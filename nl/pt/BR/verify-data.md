---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: verify data, access data, Cloud Object Storage, move data to Block Storage, move data to File Storage

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

# Verificando seus dados
{: #verify-data}

É possível acessar e verificar seus dados migrados usando o {{site.data.keyword.cos_full}}.
{: shortdesc}

Após a conclusão da transferência, aproveite o acesso imediato aos seus dados na nuvem enquanto o {{site.data.keyword.cloud_notm}} limpa o dispositivo com segurança.

## Acessando seus dados no Cloud Object Storage
{: #access-data-cos}

Seus dados migrados ficam disponíveis na instância do Cloud Object Storage especificada quando você enviou sua solicitação do {{site.data.keyword.mdms_short}}. Antes de excluir dados do seu servidor de origem, verifique se eles foram transferidos por upload com sucesso para o {{site.data.keyword.cloud_notm}}.

Para acessar e verificar seus dados: 

1. [Faça login no console do {{site.data.keyword.cloud_notm}}](https://{DomainName}/){: external}.
2. Acesse **Menu** &gt; **Lista de recursos** para visualizar uma lista de seus recursos.
3. Na lista de recursos do seu {{site.data.keyword.cloud_notm}}, selecione sua instância provisionada do Cloud Object Storage.
4. Na lista de depósitos de armazenamento disponíveis, selecione o nome do depósito designado para a migração de dados.
5. Verifique se os objetos associados ao depósito correspondem aos dados copiados para o dispositivo {{site.data.keyword.mdms_short}}.

## Movendo dados para uma solução de armazenamento diferente
{: #move-data}

Dependendo dos seus requisitos de carga de trabalho, talvez seja necessário mover seus dados migrados do Cloud Object Storage para uma solução de armazenamento em nuvem diferente, como o [File Storage](https://{DomainName}/catalog/infrastructure/file-storage) ou o [Block Storage](https://{DomainName}/catalog/infrastructure/block-storage). 

Para saber mais sobre as opções de migração de armazenamento, consulte [Receita: movendo dados do COS para o File Storage ou o Block Storage](https://developer.ibm.com/recipes/tutorials/moving-data-from-cos-to-file-or-block-storage/){: external}.

