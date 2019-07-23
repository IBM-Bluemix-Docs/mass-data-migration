---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-10"

keywords:

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
{:faq: data-hd-content-type='faq'}

# FAQs
{: #faqs}

Perguntas mais frequentes sobre o {{site.data.keyword.mdms_full}}.
{: shortdesc}

## O que é o {{site.data.keyword.mdms_full_notm}}?
{: #what-is-mdms}
{: faq}

O {{site.data.keyword.mdms_full_notm}} é um serviço de transferência física de dados que acelera a movimentação segura de terabytes ou petabytes de dados no {{site.data.keyword.cloud_notm}} por meio de dispositivos de armazenamento robustos e móveis, com 120 TB de capacidade utilizável.

## Como começo a usar o {{site.data.keyword.mdms_short}}?
{: #how-to-use-mdms}
{: faq}

Use o [{{site.data.keyword.slportal}}](https://control.softlayer.com/){: external} para enviar sua solicitação. Quando sua solicitação é aprovada e processada, o próximo dispositivo ou os dispositivos disponíveis são configurados e enviados a você com base em suas informações de rede e remessa. 

## Quem deve usar o {{site.data.keyword.mdms_short}}?
{: #who-uses-mdms}
{: faq}

De data centers e escritórios a locais remotos, como plataformas de petróleo e navios, os dispositivos {{site.data.keyword.mdms_short}} são equipados para funcionar em praticamente qualquer ambiente. O {{site.data.keyword.mdms_short}} também é uma ótima alternativa caso as opções de transferência de dados pela rede sejam muito caras, lentas ou indisponíveis.

## Quantos dados posso transferir usando o {{site.data.keyword.mdms_short}}?
{: #how-much-data}
{: faq}

Praticamente não há limites para a quantidade de dados que podem ser transferidos, sejam alguns terabytes ou muitos petabytes. Cada dispositivo contém até 120 TB de capacidade utilizável no RAID-6, mas é possível usar múltiplos dispositivos para acomodar cargas de trabalho maiores. O {{site.data.keyword.mdms_short}} também oferece a compressão sequencial, que pode aumentar ainda mais a capacidade utilizável, dependendo da capacidade de compressão de seu conjunto de dados. O maior objeto único é limitado a 10 TB de tamanho.


## Como posso usar múltiplos dispositivos para mover cargas de trabalho maiores que excedem 120 TB?
{: #using-multiple-devices}
{: faq}

Use múltiplos dispositivos em paralelo ou em uma série para mover todos os dados em uma migração única ou use um único dispositivo em migrações iterativas. Por exemplo, transfira 1 PB de dados usando nove dispositivos em paralelo ou use um único dispositivo em nove migrações separadas. Se usar diversos dispositivos em paralelo, lembre-se de que a taxa de ingestão será mais lenta.

## Quanto tempo leva para transferir meus dados?
{: #transfer-timeline}
{: faq}

A partir do momento em que um cliente envia uma solicitação do {{site.data.keyword.mdms_short}} para saber quando seus dados estarão acessíveis no depósito do IBM Cloud Object Storage, o tempo de retorno poderá ser uma questão de dias. O desempenho da transferência pode ser afetado por diversos fatores, como a rede, a largura de banda ou o número de arquivos sendo transferidos. Por exemplo, a transferência de milhões de arquivos pequenos levará mais tempo do que a transferência da mesma quantidade de dados contida em menos arquivos relativamente maiores.

## Por quanto tempo posso ter um dispositivo {{site.data.keyword.mdms_short}}?
{: #device-onsite-time}
{: faq}

Um dispositivo pode ser mantido localmente sem custo adicional nos primeiros 10 dias úteis. Isso não inclui os dias de envio ou de retorno à IBM (máximo de dois dias) de seu dispositivo. Se for necessário mais tempo para concluir sua ingestão, será possível estender seu uso por US$ 30 por dia corrido após esse período. Aplica-se a todas as regiões.

## Quais interfaces de rede são suportadas pelo {{site.data.keyword.mdms_short}}?
{: #supported-network-interfaces}
{: faq}

Os dispositivos {{site.data.keyword.mdms_short}} têm interfaces de rede de 10 Gbps com portas de rede de cobre RJ45 (CAT6a) e SFP+.

Os conversores de RJ45 para SFP+ são incluídos somente em modelos de dispositivo que não possuem conexões SFP+ nativas. Não suportamos fibra no momento.

## Qual é a opção de envio padrão do {{site.data.keyword.mdms_short}}?
{: #shipping-options}
{: faq}

O {{site.data.keyword.mdms_short}} usa a entrega de roundtrip UPS aérea em um dia útil para o envio de todos os dispositivos. O custo é incluído em uma taxa fixa baixa US$ 395 por dispositivo. Os clientes não conseguem selecionar métodos de remessa alternativos atualmente.


## Em quais regiões o {{site.data.keyword.mdms_short}} está disponível?
{: #regions-available}
{: faq}

Atualmente, o {{site.data.keyword.mdms_short}} está disponível nos Estados Unidos (EUA), na União Europeia (UE), no Japão, na Austrália, no Brasil, em Cingapura, em Hong Kong, na Noruega, na Coreia do Sul, no Canadá e no México. Uma expansão geográfica adicional está em andamento. A realização de pedidos on-line está disponível na maioria das regiões. Para qualquer região sem a realização de pedidos on-line, entre em contato com seu representante de vendas IBM para saber mais sobre como usar o serviço.

Os dispositivos não podem ser enviados para além de fronteiras internacionais (por exemplo, um dispositivo não pode ser solicitado em uma região e enviado para outra), com exceção da União Europeia e seus 28 países-membros.
{: note}

## Qual é a opção de envio padrão do {{site.data.keyword.mdms_short}} nos EUA?
{: #default-shipping-us}
{: faq}

Para dispositivos nos EUA, o {{site.data.keyword.mdms_short}} usa o envio de roundtrip UPS para o dia seguinte. O custo do envio está incluído no preço. No momento, os clientes não podem selecionar métodos de envio alternativos. 

## Qual é a opção de envio padrão do {{site.data.keyword.mdms_short}} na UE?
{: #default-shipping-eu}
{: faq}

Para dispositivos na UE, o {{site.data.keyword.mdms_short}} usa o envio de roundtrip FedEx para o dia seguinte. O custo do envio está incluído no preço. No momento, os clientes não podem selecionar métodos de envio alternativos. 

## Qual é a opção de envio padrão do {{site.data.keyword.mdms_short}} em todas as outras regiões suportadas?
{: #default-shipping-other}
{: faq}

Para todas as regiões suportadas fora dos EUA e da UE, os fornecedores e os prazos de envio variam. O custo do envio está incluído no preço. No momento, os clientes não podem selecionar métodos de envio alternativos.

Nessas regiões, a IBM não pode agendar o envio de roundtrip no momento da realização do pedido. Em vez disso, os envios unidirecionais são agendados no momento em que um envio é necessário. Para remessas de saída, aguarde pelo menos três dias úteis para que a IBM coordene o envio de seu dispositivo {{site.data.keyword.mdms_short}} após a realização da solicitação.
{: note}

Para pedidos fora dos EUA e da UE, solicite uma remessa de retorno para o dispositivo pelo menos três dias úteis antes da data na qual deseja enviá-lo. Por exemplo, se desejar enviar o dispositivo na sexta-feira, coordene uma remessa de retorno na segunda-feira da mesma semana. É possível solicitar uma remessa de retorno na guia _Detalhes da solicitação_ do painel do {{site.data.keyword.mdms_short}}.
{: important}

## Estou no Japão, na Austrália, no Brasil, no Canadá, no México, em Hong Kong, em Cingapura, na Noruega ou na Coreia do Sul. Como faço para solicitar a remessa de retorno para meu dispositivo {{site.data.keyword.mdms_short}}?
{: #shipping-timetable-other}
{: faq}

Se estiver usando o {{site.data.keyword.mdms_short}} fora das regiões dos EUA e da UE, será preciso solicitar uma remessa de retorno do dispositivo pelo menos três dias úteis antes da data desejada para seu envio. Por exemplo, se desejar enviar o dispositivo na sexta-feira, coordene uma remessa de retorno na segunda-feira da mesma semana.

## Quanto custa importar dados para o {{site.data.keyword.cloud_notm}}?
{: #data-transfer-cost}
{: faq}

Não há taxas para dados transferidos para o {{site.data.keyword.cloud_notm}}.


## Posso usar o {{site.data.keyword.mdms_short}} para exportar dados do {{site.data.keyword.cloud_notm}}?
{: #exporting-data}
{: faq}

O {{site.data.keyword.mdms_short}} não suporta a exportação de dados do {{site.data.keyword.cloud_notm}} no momento.


## O {{site.data.keyword.mdms_short}} criptografa meus dados?
{: #encryption}
{: faq}

O {{site.data.keyword.mdms_short}} criptografa todos os dados com a criptografia AES de 256 bits e fornece uma senha forte para desbloquear o conjunto de armazenamentos. Toda a transferência de dados dentro do
{{site.data.keyword.IBM}} é feita sobre SSL.

## Como o {{site.data.keyword.mdms_short}} protege fisicamente meus dados?
{: #security}
{: faq}

Todos os dispositivos {{site.data.keyword.mdms_short}} estão alojados em gabinetes robustos e duráveis. Essas caixas são à prova d'água, à prova de choque e invioláveis para garantir a segurança de roundtrip do dispositivo e dos dados.

## Como posso rastrear minha solicitação durante o processo de migração?
{: #how-to-track-request}
{: faq}

Para rastrear o status da sua solicitação, navegue até a guia _Detalhes da solicitação_ do painel do {{site.data.keyword.mdms_short}} no console do {{site.data.keyword.cloud_notm}}.

## Como meus dados são apagados do dispositivo {{site.data.keyword.mdms_short}} depois de serem transferidos para o {{site.data.keyword.cos_full_notm}}?
{: #data-erasure}
{: faq}

Assim que sua transferência de dados para o IBM Cloud Object Storage for concluída, a IBM apagará imediatamente o dispositivo usando os padrões de limpeza de dados NIST para garantir o apagamento completo de todos os dados do cliente dos dispositivos.

## Quais são as interfaces de arquivo no {{site.data.keyword.mdms_short}}?
{: #file-interfaces}
{: faq}

O {{site.data.keyword.mdms_short}} suporta os protocolos Network File System (NFS) e Bloco de Mensagens do Servidor (SMB).

## Como faço para usar a interface de arquivo no {{site.data.keyword.mdms_short}}?
{: #how-to-use-file-interface}
{: faq}

Primeiro, desbloqueie o conjunto de criptografia. Em seguida, monte o compartilhamento no servidor que contém os dados que você pretende migrar. Comece a copiar seus arquivos de dados para o compartilhamento de rede.

## Quais são os benefícios da interface de arquivo no {{site.data.keyword.mdms_short}}?
{: #file-interface-benefits}
{: faq}

A interface de arquivo é baseada no arquivo maduro e no software de rede que permite que muitos arquivos grandes sejam copiados e transportados para o {{site.data.keyword.cloud_notm}}.

## Como os arquivos são armazenados no dispositivo {{site.data.keyword.mdms_short}}?
{: #file-storage}
{: faq}

Os dispositivos {{site.data.keyword.mdms_short}} usam um sistema de arquivos ZFS com compactação LZ4 e criptografia AES de 256 bits.

## Quanto custa usar o {{site.data.keyword.mdms_short}} nos EUA?
{: #pricing-us}
{: faq}

Nos EUA, uma taxa fixa de US$ 395 é cobrada por dispositivo, incluindo a taxa de dispositivo de US$ 295, o envio de roundtrip UPS para o próximo dia de US$ 100 e 10 dias úteis de uso no local.

Seus 10 dias de uso no local não incluem os dias de envio ou de retorno à IBM (máximo de dois dias) de seu dispositivo. Se mais tempo do que os 10 dias úteis alocados for necessário para concluir sua migração, será cobrada uma taxa de extensão de US$ 30 para cada dia adicional de uso.

## Quanto custa usar o {{site.data.keyword.mdms_short}} na UE?
{: #pricing-eu}
{: faq}

Na UE, uma taxa fixa de US$ 445 é cobrada por dispositivo, incluindo a taxa de dispositivo de US$ 295, o envio de roundtrip FedEx para o próximo dia de US$ 150 e 10 dias úteis de uso no local.

Seus 10 dias de uso no local não incluem os dias de envio ou de retorno à IBM (máximo de dois dias) de seu dispositivo. Se mais tempo do que os 10 dias alocados for necessário para concluir sua migração, será cobrada uma taxa de extensão de US$ 30 para cada dia adicional de uso.

## Quanto custa usar o {{site.data.keyword.mdms_short}} em todas as outras regiões suportadas?
{: #pricing-other}
{: faq}

Em todas as outras regiões (Japão, Austrália, Brasil, Canadá, México, Hong Kong, Cingapura, Noruega e Coreia do Sul), uma taxa fixa de US$ 1.145 é cobrada por dispositivo, incluindo a taxa de dispositivo de US$ 295, o envio de roundtrip de US$ 850 e 10 dias úteis de uso no local.

Seus 10 dias de uso no local não incluem os dias de envio ou de retorno à IBM (máximo de dois dias) de seu dispositivo. Se mais tempo do que os 10 dias alocados for necessário para concluir sua migração, será cobrada uma taxa de extensão de US$ 30 para cada dia adicional de uso.

Há requisitos especiais de envio para essas regiões. Consulte as informações acima para saber mais.
{: note}

## Sou cobrado para uso do {{site.data.keyword.cos_full_notm}}?
{: #pricing-cos}
{: faq}

A transferência de dados para o {{site.data.keyword.cloud_notm}} ocorre sem nenhum custo para você. No entanto, as taxas padrão se aplicam aos dados armazenados no {{site.data.keyword.cos_full_notm}} ou em qualquer outro serviço {{site.data.keyword.cloud_notm}}. Para saber mais sobre as opções de precificação no Cloud Object Storage, consulte [Precificação do {{site.data.keyword.cos_full_notm}}](https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage){: external}. 

## Posso comprar um dispositivo {{site.data.keyword.mdms_full_notm}}?
{: #purchasing-devices}
{: faq}

Os dispositivos {{site.data.keyword.mdms_full_notm}} não estão disponíveis para compra.

## Como o processo do {{site.data.keyword.mdms_short}} mantém a exclusividade dos nomes de objeto?
{: #object-name-uniqueness}
{: faq}

Para garantir que os nomes de objetos sejam exclusivos quando copiados para um depósito do Cloud Object Storage, o caminho do arquivo inclui um prefixo no nome do objeto. Por exemplo, `/root/user/config.ini` torna-se `root/user/config.ini` quando copiado para o depósito.

## O que acontecerá se o depósito de destino não existir na conta do {{site.data.keyword.cos_full_notm}}?
{: #target-buckets}
{: faq}

Se o depósito de destino não existir, ele será criado. Se ele existir, deverá estar vazio,
caso contrário, a cópia não poderá continuar.  

## Os links são ignorados durante o processo de varredura?
{: #links-scan-process}
{: faq}

Sim. Symlinks e links físicos são ignorados durante o processo de varredura.
