---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: user permissions, manage access, IAM roles

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

# Permissões de acesso de
{: #manage-access}

O {{site.data.keyword.mdms_full}} suporta um sistema de controle de acesso centralizado, governado pelo {{site.data.keyword.iamlong}}, para ajudá-lo a gerenciar usuários e o acesso à sua solicitação do {{site.data.keyword.mdms_short}} por meio do console do {{site.data.keyword.cloud_notm}}.
{: shortdesc}

Esse recurso está disponível como parte da liberação beta do {{site.data.keyword.mdms_short}}. Para saber mais sobre como participar do programa beta, confira [Obtendo acesso à liberação beta](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta).
{: note}

## Funções e permissões
{: #roles}

Como proprietário da conta, é possível configurar políticas em sua conta do {{site.data.keyword.cloud_notm}} para criar diferentes níveis de acesso para diferentes usuários. Depois de criar uma solicitação do {{site.data.keyword.mdms_short}}, você decide quem pode rastrear o progresso do pedido no console do {{site.data.keyword.cloud_notm}}.

A tabela a seguir mostra como ações do {{site.data.keyword.mdms_short}} são mapeadas para [funções de gerenciamento de plataforma do {{site.data.keyword.cloud_notm}} IAM](/docs/iam?topic=iam-userroles#iamusermanrol). 

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>Função de gerenciamento da plataforma</th>
    <th>Descrição</th>
    <th>Exemplo de ações</th>
  </tr>
  <tr>
    <td><p>Viewer</p></td>
    <td><p>Um visualizador tem acesso somente visualização a instâncias de serviço em uma conta do {{site.data.keyword.cloud_notm}}. Os visualizadores não podem criar nem modificar instâncias de serviço.</p></td>
    <td>
      <p>
        <ul>
          <li>Acessar a página de detalhes da solicitação do {{site.data.keyword.mdms_short}}</li>
          <li>Visualizar o status de um pedido do {{site.data.keyword.mdms_short}}</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Operador</p></td>
    <td><p>Um operador pode visualizar instâncias de serviço, gerenciar aliases, ligações e credenciais de serviço.</p></td>
    <td>
      <p>
        <ul>
          <li>Não aplicável</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Editor</p></td>
    <td><p>Um editor tem permissões que vão além da função de operador, incluindo a capacidade de criar e excluir instâncias de serviço.</p></td>
    <td>
      <p>
        <ul>
          <li>Criar uma solicitação do {{site.data.keyword.mdms_short}}.</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>Administrador</p></td>
    <td><p>Um gerenciador pode executar todas as ações que um visualizador, um operador e um editor executam, incluindo a capacidade de convidar novos usuários e designar políticas de acesso a outros usuários.</p></td>
    <td>
      <p>
        <ul>
          <li>Todas as ações que um visualizador, um operador e um editor podem executar</li>
          <li>Designar políticas de acesso de usuário</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">Tabela 1. Descreve como as funções de identidade e acesso são mapeadas para permissões do {{site.data.keyword.mdms_short}}</caption>
</table>

Para obter informações sobre como designar funções de usuário na IU, consulte [Gerenciando acesso aos recursos](/docs/iam?topic=iam-iammanidaccser#iammanidaccser).
{: tip}



