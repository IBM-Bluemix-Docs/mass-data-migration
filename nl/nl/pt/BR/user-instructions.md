---

copyright:
  years: 2018
lastupdated: "2018-04-06"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# Instruções do usuário

## Visão geral

O dispositivo {{site.data.keyword.cloud}} Mass Migration é um dispositivo de
armazenamento móvel capaz de apresentar armazenamentos NFS ou CFS montáveis e é gerenciado por meio de
uma interface do navegador da web.  O dispositivo é enviado para um cliente, carregado com dados no local e,
em seguida, devolvido para um data center do {{site.data.keyword.BluSoftlayer_full}} e
carregado no {{site.data.keyword.cos_full}} na conta do cliente e em um depósito.


### Energia

O dispositivo é enviado com um cabo de energia C13-US
[https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Se o dispositivo estiver sendo utilizado fora dos Estados Unidos, um adaptador de energia poderá ser
necessário.

O dispositivo aceita todos os intervalos de alimentação padrão.
![Intervalo de alimentação](/images/PowerRating.png)


### Conectividade Ethernet

Há duas conexões Ethernet a serem feitas.  Uma para gerenciamento de dispositivo por meio de um navegador
e outra para a movimentação de dados na mesma sub-rede na qual os dados de origem residem.

Ambas as portas se originam do dispositivo como RJ45 e os cabos CAT6A são fornecidos.  Adaptadores
SFP+ de cobre são fornecidos para converter de RJ45.  É garantido que os adaptadores funcionam
com todos os fabricantes de comutador. Esses adaptadores estão localizados em um depósito na parte de baixo da
tampa de remessa.

Eth1 (1 GbE-B) é usado para gerenciamento de dispositivo e, como tal, deve ter um gateway especificado na
configuração de endereço IP.  Isso pode ser visualizado por meio do LCD depois que o dispositivo é ligado
(consulte o anexo de configuração de endereço IP abaixo).

Eth3 (10 GbE-B) é usado para a transferência de dados.  Essa conexão deve estar na mesma sub-rede que
os dados de origem ou pode ser conectada diretamente ao servidor, se necessário.

Se um fator de forma diferente de conexão Ethernet for necessário, o cliente deverá fornecer o conversor.



## Instruções passo a passo do usuário

1.	O dispositivo chega pré-configurado com seu endereço IP, nome de usuário, conjuntos travados e
compartilhamento NFS.  A senha do usuário e a senha do conjunto de armazenamentos serão comunicadas por e-mail
separado.

2.	Determine o local mais apropriado para colocar o dispositivo; em que ele alcançará as
conexões de energia e de Ethernet (1 GbE e 10 GbE) e minimizará o fluxo de pessoas.

3.	Posicione o dispositivo a ser conectado; ele pode continuar na caixa de transporte durante o
uso. Assegure-se de que o dispositivo esteja em temperatura ambiente e que não haja condensação nele. Conecte
a energia usando o cabo de energia fornecido sob a tampa da caixa e ligue o dispositivo.<br/>
    **Nota**: há dois comutadores de energia.
![Comutadores de energia](/images/MDMSPowerSwitch.png)
    **Nota**: o dispositivo não precisa ser removido da caixa móvel.

4.	Remova o cabo CAT6A da tampa da caixa e conecte-o à porta Eth3 (10 GbE-B), conforme mostrado na
figura abaixo.
![](/images/MDMSNewEth1and3.png)

5.	Conecte o adaptador CAT6A para SFP+ fornecido e conecte seu comutador 10 Gb.

6.	Se o endereço IP configurado para Eth3 puder ser acessado por meio do navegador
HTTPS://'Your-Eth3-IPAddress', continue com a próxima etapa, caso contrário, conecte a porta Eth1 (1 GbE-B).<br/>
    **Nota**: consulte o Anexo de Configuração IP abaixo se você precisar
mudar quaisquer configurações IP para Eth3 ou Eth1.

7. Abra seu navegador e insira HTTPS://'Your-Eth1-IPAddress'. Insira Eth1 conforme apropriado para sua
configuração de rede. Aceite a exceção de certificado.

8.	Use o nome de usuário e a senha para efetuar login.<br/>
    ![Página de login](/images/Login.png)

9.  O assistente de fluxo de trabalho apresenta acesso aos itens específicos geralmente usados em ordem
da esquerda para a direita.  <br/>
    ![Ícones do fluxo de trabalho](/images/workflow.png) <br/>
    **NOTA**: o fluxo de trabalho pode ser reaberto usando o botão
Gerenciador de fluxo de trabalho na parte superior esquerda da GUI.

10.	Ative o conjunto de armazenamentos pré-configurado:
    - Clique em **Desbloquear e iniciar o conjunto de armazenamentos**.
    - Insira sua passphrase do conjunto de armazenamentos e clique em **OK**.
![Ativar conjunto de armazenamentos](/images/UnlockPool.png)

11. Por padrão, o compartilhamento tem os protocolos NFS e SMB ativados sem restrições de acesso
e são colocados no compartilhamento. Para restringir o acesso a este compartilhamento (para NFS e/ou SMB), clique
com o botão direito no nome de compartilhamento e selecione o item de menu apropriado.<br/>
    ![Restringir acesso de compartilhamento](/images/ShareControls.png)

12. Depois que o conjunto de armazenamentos é ativado, o compartilhamento NFS se torna disponível para
montagem.  No fluxo de trabalho, clique em **Visualizar compartilhamentos de rede** para
abrira a visualização de compartilhamentos de rede.  Feche o fluxo de trabalho, clique com o botão direito
no compartilhamento e selecione comando de montagem para ver as informações de nome de compartilhamento e de
montagem. Monte o compartilhamento em seu servidor de origem e carregue os dados. Certifique-se de especificar o endereço IP do link de 10 Gb ao montar o compartilhamento.     ![Montando o compartilhamento](/images/MountCommand.png)

13. Comece a copiar seus dados para o compartilhamento NFS. No fluxo de trabalho, clique em **Visualizar atividade de rede** para mostrar o carregamento de Ethernet de entrada na GUI à medida que os dados são transferidos para o dispositivo no link de 10 Gb.
    ![Visualizar atividade](/images/UserGuide13.png)

14. No fluxo de trabalho, clique em **Visualizar conjunto de armazenamentos** para monitorar o uso de armazenamento e o IOPS no dispositivo.
    ![Visualizar conjunto de armazenamentos](/images/UserGuide14.png)

15.	Quando o carregamento for concluído, desligue normalmente o sistema. No fluxo de trabalho, clique em **Encerrar dispositivo...**.  
    ![Encerrando o dispositivo](/images/Shutdown.png)

16.	Desconecte o dispositivo e retorne o cabo de energia, o cabo Ethernet e o adaptador SFP+ para seus respectivos locais de armazenamento sob a tampa.

17.	Anexe o rótulo de remessa fornecido, notifique o remetente e devolva o dispositivo para o data center para carregá-lo no armazenamento de objeto de nuvem.


## Anexo de configuração de endereço IP
O painel de LCD na parte superior do dispositivo pode ser usado para configurar os endereços IP para as portas Ethernet.
É possível navegar no painel de LCD usando os botões Para cima, Para baixo, Voltar/ESC e Para frente/ENTER. Com a tecla Enter leva você para um menu e com a opção Sair você sai de lá.

Ao editar um endereço IP ou máscara de sub-rede, Enter avança você um caractere por vez e Sair o retrocede um caractere por vez. Para cima e Para baixo alterna pelos números do local escolhido.
Use Sair para volta ao menu anterior.  

Navegue para baixo até o item de menu “Atualizar...” e pressione Enter para salvar a configuração.

  ![](/images/MDMSLCD.png)
