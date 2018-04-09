---

copyright:
  years: 2017
lastupdated: "2017-12-15"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Introdução ao {{site.data.keyword.cloud_notm}} Mass Data Migration

## O que é necessário ao solicitar um dispositivo

1. Configurações de rede para o dispositivo de armazenamento
   - Endereço IP estático
   - Máscara de rede para ativação da transferência de dados
2. Configurações de rede para computador remoto
   - Endereço IP estático
   - Máscara de rede 
   - Gateway padrão para acessar a interface com o usuário
3. Destino de download do armazenamento de objeto de nuvem <br/>
   **Importante**: é necessário ter pelo menos uma conta do {{site.data.keyword.cos_full}} e um depósito em um local para Várias regiões dos EUA ou Sul dos EUA para concluir o formulário de solicitação. Se você ainda não tiver uma conta do {{site.data.keyword.cos_full_notm}}}, crie uma antes de solicitar o dispositivo Mass Data Migration. Consulte [Sobre o {{site.data.keyword.cos_full}}](https://console.bluemix.net/docs/services/cloud-object-storage/about-cos.html){:new_window}.

## Etapa 1: criar uma solicitação

1. Acesse o [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} usando suas credenciais exclusivas.
2. Selecione **Armazenamento** > **Migração de dados** > **Mass Data Migration** na Barra de navegação para acessar a página de entrada do Mass Data Migration. <br/>
![Opção de serviço de transferência de dados no menu do Portal do cliente](/images/DTSinControlMenu.PNG) <br/>
3. Clique no link **Solicitar dispositivo** para abrir o formulário da solicitação.
4. Preencha cada campo no formulário do pedido **Mass Data Migration**.
   - **Endereço de entrega**: esse formulário não é preenchido e cada campo é editável. Forneça o nome da pessoa que aceitará a entrega do dispositivo no campo Atenção. Ao selecionar o local de entrega, considere o peso do dispositivo (66 libras incluindo a caixa) e acessibilidade. <br/> (**Nota**: o dispositivo é equipado com rodas e com uma alça suspensa para manobras).
   - **Contatos de migração de chave**: esse formulário não está preenchido. Cada campo é editável. Mais de uma pessoa pode ser incluída. 
   - **Configuração de rede do data center**: forneça detalhes de configuração de rede para o pré-fornecimento da porta Eth3 no dispositivo Mass Data Migration antes da remessa.
   - **Destino de transferência de dados**: selecione sua conta de destino existente na lista suspensa.
   - **Nome da solicitação**: insira um nome para ajudar a rastrear seu pedido.
5. Marque a caixa de seleção **Eu li e concordo com os termos completos do contrato do Massa Data Migration** após ler cada contrato de serviço fornecido.
6. Clique em **Fazer solicitação** para enviar a solicitação. Clique em **Cancelar** para abandonar completamente o formulário e retornar para a página de entrada do Mass Data Migration.


## Etapa 2: preparar e enviar

Após enviar a solicitação, o status para o chamado de solicitação aparecerá como *Processando a solicitação*. Quando sua solicitação tiver sido processada, o {{site.data.keyword.IBM}} iniciará a pré-configuração do próximo dispositivo disponível e o status na grade [Solicitações](https://control.softlayer.com/storage/mdms){:new_window} mostrará *Preparando dispositivo* seguido por *Aguardando remessa*.

Quando o pedido é aceito e o dispositivo está sendo preparado, o status na grade [Solicitações](https://control.softlayer.com/storage/mdms){:new_window} mostra *Preparando dispositivo* seguido por *Aguardando remessa*. Quando sua solicitação entra no status *Aguardando remessa*, ela não pode mais ser cancelada. 

Quando o dispositivo é retirado em loja pela transportadora para ser enviado para o seu local, o status da Solicitação é atualizado para *Dispositivo enviado*. O número de rastreamento será compartilhado com você na seção **Detalhes do pedido** da grade [Solicitações](https://control.softlayer.com/storage/mdms){:new_window}.


## Etapa 3: receber e conectar

1. O dispositivo chega pré-configurado para você. Uma [instrução de ligação/conexão](user-instructions.html) básica será incluída.<br/>
  **Nota**: o nome de usuário e a senha do conjunto de armazenamentos serão fornecidos separadamente. Verifique os **Detalhes da solicitação** em sua grade [Solicitações](https://control.softlayer.com/storage/mdms){:new_window} para obter as credenciais.
2. Aponte seu navegador para o endereço IP estático fornecido no formulário do pedido.
3. Efetue login e forneça a senha para desbloquear o conjunto de armazenamentos vazio. <br/>
   **Nota**: consulte os Detalhes da solicitação de sua grade [Solicitações](https://control.softlayer.com/storage/mdms){:new_window} para a senha.
4. Monte o compartilhamento NFS em seu servidor.
5. Execute novamente seu inventário do DataShuttle para assegurar que quaisquer novos arquivos que possam ter sido criados após o aplicativo sejam capturados.

## Etapa 4: receber e conectar
1. Execute a cópia DataShuttle para mover os dados.
2. Bloquear o conjunto de armazenamento.
3. Encerre normalmente o dispositivo Mass Data Migration.
4. Envie a caixa de volta para o data center do {{site.data.keyword.BluSoftlayer_full}} usando o rótulo de remessa fornecido.

Quando o dispositivo é devolvido para o {{site.data.keyword.BluSoftlayer}}, o status da solicitação muda para *Dispositivo recebido*. 

## Etapa 5: transferência e acesso

Durante o processo de transferência, o status da solicitação é exibido como *Transferência de dados*. O status muda novamente quando a migração para o depósito do {{site.data.keyword.objectstorageshort}} é concluída (*Transferência concluída*). Seus dados se tornam acessíveis imediatamente quando a transferência de alta velocidade para seu depósito do armazenamento de objeto de nuvem é concluída.

## Etapa 6: apagar dispositivo

O {{site.data.keyword.IBM}} implementará requisitos de limpeza de dados no nível DOD para apagar permanentemente seus dados do dispositivo. Quando concluído, o status da solicitação exibe *Apagamento concluído*.

## Notas adicionais

### Exclusividade no depósito

Para assegurar que os nomes de objetos sejam exclusivos quando eles são copiados para o depósito, o caminho de arquivo recebe um prefixo no nome do objeto; `/root/user/config.ini` se torna "root/user/config.ini" quando copiado para o depósito.

### Depósitos

Se o depósito de destino não existe, ele é criado.  Se ele existe, deve estar vazio, caso contrário, a cópia não pode continuar.  

### Sistemas de arquivos

Symlinks e Hardlinks são ignorados durante o processo de varredura.