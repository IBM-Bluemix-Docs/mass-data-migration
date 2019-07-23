---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords: unable to view order, unable to mount SMB share

subcollection: mass-data-migration

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve}
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

# Detectando Problemas
{: #troubleshooting}

Problemas gerais com o uso do {{site.data.keyword.mdms_full}} podem incluir a visualização do status de seu pedido ou o acesso à interface com o usuário. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{: shortdesc}

## Não é possível conectar-se ao compartilhamento do SMB
{: #unable-to-mount-smb-share}

Quando você tenta montar o compartilhamento do Bloco de Mensagens do Servidor (SMB) provisionado no dispositivo {{site.data.keyword.mdms_short}}, não é possível conectar-se a ele. 

Você está usando o protocolo de transferência de arquivos do SMB em um servidor Windows associado a um domínio do Active Directory. Para mover dados para o dispositivo {{site.data.keyword.mdms_short}}, é necessário se conectar ao compartilhamento de rede provisionado no dispositivo. É possível executar ping no endereço IP que corresponde à porta de transferência de dados de 10 GbE no dispositivo, mas não é possível montar ou se conectar ao compartilhamento por meio de seu servidor.
{: tsSymptoms}

Depois de associar o dispositivo {{site.data.keyword.mdms_short}} ao Active Directory, o sistema ativa a assinatura do SMB por padrão. A assinatura do SMB inclui segurança adicional durante uma comunicação de rede, eliminando a possibilidade de ataques man-in-the-middle. No entanto, a assinatura do SMB pode afetar o desempenho de rede para sua transferência de dados ou causar [problemas na montagem do compartilhamento para o seu servidor](https://support.osnexus.com/hc/en-us/articles/360028195772-Connection-issues-to-SMB-share-after-joining-an-AD-domain){: external}.
{: tsCauses} 

Se você não usa nem exige a assinatura do SMB para seu ambiente, é possível desativá-la no cliente para evitar problemas de conexão e aumentar o desempenho da sua transferência de dados.
{: tsResolve}

Para desativar a assinatura do SMB em um servidor Windows, configure as seguintes chaves de registro para zero:

```
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\LanmanServer\Parameters\"requiresecuritysignature"=dword:00000000
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\Lanmanworkstation\Parameters\"requiresecuritysignature"=dword:00000000 
```
{: screen}

Para saber mais sobre a assinatura do SMB, consulte [Visão geral da assinatura do Bloco de Mensagens do Servidor](https://support.microsoft.com/en-us/help/887429/overview-of-server-message-block-signing){: external}.

## Não é possível ver detalhes do pedido
{: #unable-to-view-order}

Quando você acessa o console do {{site.data.keyword.cloud_notm}}, não é possível visualizar ou rastrear um pedido do {{site.data.keyword.mdms_short}} para sua organização.

É possível ver uma lista de serviços na sua lista de recursos do {{site.data.keyword.cloud_notm}}, mas não é possível ver uma entrada do {{site.data.keyword.mdms_short}}.
{: tsSymptoms}

Você não tem a autorização correta para visualizar ou rastrear pedidos do {{site.data.keyword.mdms_short}}.
{: tsCauses} 

Verifique com o seu administrador se você está designado com a função correta no grupo de recursos aplicável ou na instância de serviço. Para obter mais informações sobre funções, veja [Funções e permissões](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-manage-access#roles).
{: tsResolve}

## Obtendo ajuda e suporte
{: #getting-help}

Se tiver problemas ou dúvidas ao usar o dispositivo {{site.data.keyword.mdms_short}}, será possível obter ajuda procurando informações no Centro de Suporte ou entrando em contato diretamente conosco.

Para acessar o Centro de suporte, efetue login no console do {{site.data.keyword.cloud_notm}} e clique em **Suporte** na barra de menus.

É possível usar o campo de procura do Centro de suporte para localizar respostas para suas perguntas na documentação do {{site.data.keyword.cloud_notm}} e fórum do Stack Overflow. Também é possível gerenciar casos de suporte por meio do Centro de suporte. É possível localizar links para o fórum do Stack Overflow, para perguntas técnicas, e para o fórum do IBM Developer Answers, para todas as outras perguntas, na seção Fóruns do Centro de Suporte.

Se você tiver um [plano de suporte](/docs/get-support?topic=get-support-support-plans#support-plans) básico, avançado ou premium, será possível localizar os números de chamada e uma opção de bate-papo para obter ajuda.

Embora o Centro de Suporte seja o método preferencial para obter suporte, se você não conseguir efetuar login no {{site.data.keyword.cloud_notm}}, será possível usar o [Portal de Serviço do {{site.data.keyword.cloud_notm}}](http://www.ibm.biz/bluemixsupport){: external} para enviar um caso.

Para obter mais informações sobre a abertura de um chamado de suporte do {{site.data.keyword.IBM_notm}} ou os níveis de suporte e as severidades de chamado, consulte [Entrando em contato com o suporte](/docs/get-support?topic=get-support-getting-customer-support){: external}.
