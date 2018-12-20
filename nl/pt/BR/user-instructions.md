---

copyright:
  years: 2018
lastupdated: "2018-10-31"

---
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Importando dados para o dispositivo IBM Cloud Mass Migration

O dispositivo {{site.data.keyword.cloud}} Mass Migration é um dispositivo de armazenamento móvel capaz de apresentar compartilhamentos do Network File System (NFS) ou do FileNet Content Federations Services (CFS). O dispositivo é gerenciado por meio de uma interface do navegador da web. O dispositivo é enviado para seu data center, carregado com dados no local, em seguida, retornado para um data center do {{site.data.keyword.BluSoftlayer_full}} e carregado em sua conta do {{site.data.keyword.cos_full}}.


## Ligando o dispositivo

O dispositivo é enviado com um cabo de energia C13-US [https://en.wikipedia.org/wiki/IEC_60320](https://en.wikipedia.org/wiki/IEC_60320){:new_window}. Se o dispositivo for usado fora dos Estados Unidos, um adaptador de energia poderá ser necessário.

O dispositivo aceita todos os intervalos de alimentação padrão.
<br/>
![Intervalo de alimentação](/images/PowerRating.png)

Para ligar o dispositivo, execute as etapas a seguir.
1. Ligue o comutador Mains ao lado do plugue de energia. <br/>
   ![Mains Switch](/images/MDMSPowerOnOff.png)

2. Use o botão Ligar/desligar sistema que está ao lado dos LEDs do link de conexão.
   ![Ligar/desligar sistema](/images/MDMSSystemOnOff.png)

O dispositivo é ligado quando o ID do sistema é mostrado na tela de LED.


## Configurando a conectividade Ethernet

Você precisa fazer duas conexões Ethernet. Uma conexão é para gerenciamento de dispositivo por meio de um navegador e a outra conexão é para movimentação de dados na mesma sub-rede na qual os dados de origem estão localizados.

O {{site.data.keyword.cloud}} fornece dois modelos do Dispositivo MDMS. Um modelo suporta apenas a conectividade RJ45. O outro modelo suporta o SFP+ de cobre e o RJ45. Dependendo do modelo do dispositivo MDMS, siga as instruções que forem apropriadas.

Por padrão, o recurso de quadros gigante está ativado nas portas de 10 GbE. Essa configuração pode ser mudada usando a opção Modificar Porta de Rede, na interface do usuário.
{:tip}

### Configurando Apenas RJ45

![RJ45](/images/RJ45PortZoom.png)

As portas se originam do dispositivo como RJ45 e os cabos CAT6A são fornecidos. Adaptadores
SFP+ de cobre são fornecidos para converter de RJ45. Os adaptadores funcionam com todos os fabricantes de comutador. Esses adaptadores estão localizados em um bolso na parte de baixo da tampa do contêiner de remessa.

- O Eth1 (`1GbE-B`) geralmente é usado para gerenciamento de dispositivo e, como tal, deve ter um gateway especificado na configuração de endereço IP. Essas informações podem ser visualizadas na tela LCD depois que o dispositivo estiver ligado (consulte a seção de configuração do endereço IP). Essa porta é usada para tornar a UI baseada na web disponível fora da sub-rede de dados.

- O Eth3 (`10GbE-B`) é usado para transferência de dados e também pode ser usado para gerenciamento de dispositivo. Essa conexão deve estar na mesma sub-rede que os dados de origem ou pode ser conectada diretamente ao servidor, se necessário.


### Configurando o Copper SFP + e o RJ45

![Copper SFP+](/images/sfp-ports-sized-port5.png)

As portas se originam do dispositivo como SFP+ de cobre e RJ45. Ambos os cabos, CAT6A e SFP+ de cobre, são fornecidos.

- O Eth5 (`10Gb SFP+ (5)`) geralmente é usado para transferência de dados, mas também pode ser usado para gerenciamento de dispositivo. Esta porta é executada apenas a 10 GbE de velocidade.

- O Eth2 (`10-GbE (2)`) geralmente é usado para gerenciamento de dispositivo, mas também pode ser usado para transferência de dados. Essa porta pode ser executada em velocidades de 1 ou 10 GbE.


A conexão de transferência de dados deve estar na mesma sub-rede que os dados de origem ou ser conectada diretamente ao servidor.

As configurações de IP podem ser visualizadas e gerenciadas na tela LCD depois que o dispositivo for ligado (consulte a seção de configuração de endereço IP).

NÃO é necessário configurar e usar ambas as portas quando o IP da porta de 10 GbE pode ser acessado por meio de um navegador da web.
{:note}


## Carregando os dados

1.	O dispositivo chega pré-configurado com o endereço IP, o nome do usuário, o conjunto de armazenamentos bloqueado e o compartilhamento do NFS. A senha de usuário e a senha do conjunto de armazenamentos são comunicadas por meio de um e-mail separado.

2.	Determine o local mais apropriado para que o dispositivo seja colocado. Ele precisa atingir ambas as conexões de energia e Ethernet e minimizar o tráfego de pessoas.

3.	Posicione o dispositivo a ser conectado. O dispositivo não precisa ser removido da caixa móvel. Ele pode permanecer na caixa de transporte durante o uso. Assegure-se de que o dispositivo esteja à temperatura ambiente e não haja condensação nele. Conecte a energia usando o cabo de energia fornecido sob a tampa da caixa e ligue o dispositivo.<br/>
    
    Observe os dois comutadores de energia.
    {:note}
    ![Comutadores de energia](/images/MDMSPowerSwitch.png)

4. Conecte o dispositivo à rede.
    - Conectando RJ45
      1. Remova o cabo CAT6A da tampa da caixa e conecte-o à porta Eth3 (10 GbE-B).
         ![Portas do dispositivo MDMS](/images/MDMSNewEth1and3.png)
      2. Conecte o CAT6A fornecido ao adaptador SFP+ e ligue em seu comutador de 10 Gb.
      3. Se o endereço IP que estiver configurado para Eth3 puder ser atingido no navegador por meio de `HTTPS://'Your-Eth3-IPAddress'`, continue com a próxima etapa. Caso contrário, conecte a porta Eth1 (`1GbE-B`).<br/>
         
         Se você precisar alterar alguma configuração IP para Eth3 ou Eth1, consulte a seção [Configurando endereços IP](#configuring-ip-addresses).
         {:tip}
         
    - Conectando o SFP de Cobre
      1. Remova o cabo SFP+ de cobre da tampa da caixa e conecte-o ao Eth5 10 GbE (5)
         ![Portas do dispositivo MDMS](/images/sfp-ports-sized-ports-labeled.png)
      2. Conecte o cabo SFP+ de cobre ao seu comutador de 10 Gb.
      3. Se o endereço IP que está configurado para o Eth5 puder ser alcançado por meio do navegador `HTTPS://'Your-Eth5-IPAddress'`, continue com a próxima etapa, caso contrário, conecte a porta Eth2 (`10GbE-B` ou `1GbE-B`).

         Se você precisar alterar alguma configuração IP para Eth5 ou Eth2, consulte a seção [Configurando endereços IP](#configuring-ip-addresses).
         {:tip}

5. Abra o navegador e insira  ` HTTPS: //Your-Eth1-IPAddress `. Substitua `Your-Eth1-IPAddress` pelo Eth1 para sua configuração de rede. Aceite a exceção de certificado.

6. Use o nome do usuário e a senha fornecidos para efetuar login.<br/>
    ![Página de login](/images/login.png)

7. O assistente de fluxo de trabalho apresenta acesso aos itens específicos que são geralmente usados em ordem da esquerda para a direita.<br/>
    ![Ícones do fluxo de trabalho](/images/workflow.png)

    O fluxo de trabalho pode ser reaberto usando o **Workflow Manager** na área superior esquerda da interface.     {:tip}

8.	Ative o conjunto de armazenamentos pré-configurado.
    - Clique em **Desbloquear e iniciar o conjunto de armazenamentos**.
    - Insira sua passphrase do conjunto de armazenamentos e clique em **OK**.
      ![Ativar conjunto de armazenamentos](/images/Unlock.png)

9. Por padrão, o compartilhamento tem os protocolos NFS e SMB que são ativados sem restrições de acesso. Para restringir o acesso a esse compartilhamento (para NFS ou SMB), clique com o botão direito no nome de compartilhamento e selecione o item de menu apropriado.<br/>
   ![Restringir acesso de compartilhamento](/images/ShareAccessControl.png)

10. Quando o conjunto de armazenamentos é ativado, o compartilhamento do NFS se torna disponível para montagem. No fluxo de trabalho, clique em **Visualizar compartilhamentos de rede** para
abrira a visualização de compartilhamentos de rede. Feche o fluxo de trabalho, clique com o botão direito no compartilhamento e selecione o comando de montagem para ver o nome de compartilhamento e as informações de montagem. Monte o compartilhamento em seu servidor de origem. Certifique-se de especificar o endereço IP do link de 10 GB.
    ![Montando o compartilhamento](/images/MountCommand.png)

11. Copie seus dados para o compartilhamento do NFS. No fluxo de trabalho, clique em **Visualizar atividade de rede** para mostrar o carregamento Ethernet de entrada à medida que dados são transferidos para o dispositivo no link de 10 GB.
    ![Visualizar atividade](/images/SystemNetworkPerf.png)

12. No fluxo de trabalho, clique em **Visualizar conjunto de armazenamentos** para monitorar o uso de armazenamento e o IOPS no dispositivo.
    ![Visualizar conjunto de armazenamentos](/images/SystemStoragePoolPerf.png)

13.	Quando o carregamento for concluído, será possível desligar o sistema normalmente. No fluxo de trabalho, clique em **Encerrar dispositivo...**.
    ![Encerrando o dispositivo](/images/SystemShutdown.png)

14.	Desconecte o dispositivo, retorne o cabo de energia, o cabo Ethernet e o adaptador SFP+ em seus locais de armazenamento sob a tampa.

16.	Anexe a etiqueta de remessa fornecida, notifique a transportadora e retorne o dispositivo para o data center.


## Configurando endereços IP

A tela LCD no dispositivo pode ser usada para configurar os endereços IP para as portas Ethernet. Você move o cursor em torno do painel LCD usando os botões **Para cima**, **Para baixo**, **Voltar/ESC** e **Avançar/ENTER**. **Enter** leva para um menu e **Sair** leva você a sair.

Ao editar um endereço IP ou máscara de sub-rede, **Enter** faz você avançar um caractere por vez; **Sair** faz voltar um caractere por vez.

**Para cima** e **Para baixo** alternam pelos números do local escolhido.

Use **Sair** para fazer backup para o menu anterior.

Acesse **Atualizar...** e pressione **Enter** para salvar a configuração.

  ![Monitor LCD](/images/MDMSLCD.png)
