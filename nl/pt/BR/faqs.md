---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-05"

---
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}


# FAQs
{: #faqs}

## O que é o {{site.data.keyword.cloud_notm}} Mass Data Migration?

O {{site.data.keyword.cloud}} Mass Data Migration é um serviço de transferência de dados físicos que acelera o movimento seguro de terabytes para petabytes de dados no {{site.data.keyword.cloud_notm}} usando dispositivos de armazenamento móvel reforçados e de capacidade utilizável de 120 TB.

<hr/>

## Como é iniciado o Mass Data Migration?
{: faq}

Use o console do [{{site.data.keyword.cloud_notm}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://{DomainName}/catalog/){:new_window} para enviar sua solicitação. Quando sua solicitação é aprovada e processada, o próximo dispositivo ou os dispositivos disponíveis são configurados e enviados a você com base em suas informações de rede e remessa. Use o link a seguir para começar agora: https://control.softlayer.com/storage/mdms

<hr/>

## Por que usar o Mass Data Migration?
{: faq}

Os dispositivos Mass Data Migration estão equipados para serem executados em quase qualquer ambiente, de data centers e escritórios a locais remotos, armazéns e navios. O Mass Data Migration também será uma alternativa se as opções de transferência de dados via rede forem de custo proibitivo, muito lentas ou indisponíveis.

<hr/>

## Qual é a quantidade de dados que pode ser transferida usando o Mass Data Migration?

Praticamente não há nenhum limite para a quantia de dados que pode ser transferida, sejam alguns terabytes até petabytes. Cada dispositivo contém até 120 TB de capacidade utilizável no RAID-6, mas é possível usar múltiplos dispositivos para acomodar cargas de trabalho maiores. O maior objeto único é limitado a 10 TB.

<hr/>

## É possível usar múltiplos dispositivos para mover cargas de trabalho maiores, que excedem os 120 TB? Se sim, como? 
{: faq}

Use múltiplos dispositivos em paralelo ou em uma série para mover todos os dados em uma migração única ou use um único dispositivo em migrações iterativas. Por exemplo, transfira 1 PB de dados usando nove dispositivos em paralelo ou use um único dispositivo em nove migrações separadas.

<hr/>

## Quanto tempo leva para transferir os dados?
{: faq}

Desde o momento em que um cliente envia uma solicitação do Mass Data Migration até quando seus dados se tornam acessíveis no depósito do {{site.data.keyword.cos_full}}, o tempo de retorno pode ser apenas sete dias. O desempenho da transferência é afetado pelo número de arquivos a serem transferidos. A transferência de milhões de arquivos pequenos leva mais tempo do que a mesma quantia de dados contidos em poucos arquivos.

<hr/>

## Por quanto tempo o dispositivo de Mass Data Migration pode ser mantido?

Um dispositivo pode ser mantido no local sem nenhum custo pelos primeiros 10 dias úteis. Esse prazo não inclui o dia em que seu dispositivo é enviado ou o dia em que você o recebe. Se mais tempo for necessário para concluir sua ingestão, será possível estender seu uso por US$ 30 por dia posteriormente (aplica-se a regiões dos EUA e da UE).

<hr/>

## Quais interfaces de rede o Mass Data Migration suporta?
{: faq}

Os dispositivos de Mass Data Migration têm interfaces de rede de 10 Gbps com portas de rede de cobre RJ45 (CAT6a) e SFP+. O conversor de RJ45 para SFP+ está incluso. Os quadros gigantes são ativados nas interfaces de 10 Gbps.

<hr/>

## Qual é a opção de envio padrão do Mass Data Migration?
{: faq}

O Mass Data Migration usa Entrega aérea em um dia útil de roundtrip da UPS para enviar todos os dispositivos. O custo é incluído em uma taxa fixa baixa US$ 395 por dispositivo. Os clientes não conseguem selecionar métodos de remessa alternativos atualmente.

<hr/>

## Em quais regiões o Mass Data Migration está disponível?
{: faq}

O Mass Data Migration está disponível somente nos Estados Unidos e na União Europeia. Todos os dados são migrados para o {{site.data.keyword.cos_full}} na Região Cruzada Padrão dos EUA ou nas camadas de Região Cruzada da UE do serviço. Os dispositivos não podem ser enviados de uma região e retornados para outra região.

<hr/>

## Quanto custa para importar dados para dentro do {{site.data.keyword.cloud_notm}}?
{: faq}

Nenhuma taxa é incorrida para dados que são transferidos para o {{site.data.keyword.cloud_notm}}.

<hr/>

## O Mass Data Migration pode ser usado para exportar dados para fora do {{site.data.keyword.cloud_notm}}?
{: faq}

O Mass Data Migration não suporta a exportação de dados fora do {{site.data.keyword.cloud_notm}} atualmente.

<hr/>

## O Mass Data Migration criptografa os dados?
{: faq}

O Mass Data Migration criptografa todos os dados com a criptografia AES de 256 bits e fornece uma senha forte para desbloquear o conjunto de armazenamentos. Toda a transferência de dados dentro do
{{site.data.keyword.IBM}} é feita sobre SSL.

<hr/>

## De que maneira o Mass Data Migration protege os dados fisicamente?
{: faq}

Todos os dispositivos do Mass Data Migration são alojados em gabinetes resistentes e duráveis. Essas caixas são à prova d'água, à prova de choque e invioláveis para garantir a segurança de roundtrip do dispositivo e dos dados.

<hr/>

## De que maneira a solicitação pode ser rastreada ao longo de todo o processo de migração?

Para rastrear o status de sua solicitação, consulte a seção de solicitações ativas na página do Mass Data Migration no [{{site.data.keyword.slportal}} ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")](https://control.softlayer.com/){:new_window}. É possível conectar-se ao portal usando o link a seguir: https://control.softlayer.com/storage/mdms ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")

<hr/>

## De que maneira os dados são apagados após terem sido transferidos ao {{site.data.keyword.cos_full_notm}}?

Assim que a transferência de seus dados para o {{site.data.keyword.cos_full}} é concluída, o {{site.data.keyword.IBM}} inicia imediatamente uma limpeza de dados de nível DOD de quatro etapas para apagar permanentemente seus dados do dispositivo.

<hr/>

## Qual é a interface de arquivo?
{: faq}

O dispositivo Mass Data Migration tem o recurso de compartilhamentos com o Network File System (NFS) e o Bloco de Mensagens do Servidor (SMB) ativado por padrão.

<hr/>

## De que maneira a interface de arquivo é usada?
{: faq}

Primeiro, desbloqueie o conjunto de criptografia. Em seguida, monte o compartilhamento no servidor que contém os dados que você pretende migrar. Inicie a cópia de seus arquivos de dados para o compartilhamento.

<hr/>

## Quais são os benefícios da interface de arquivo no Mass Data Migration?
{: faq}

A interface de arquivo é baseada no arquivo maduro e no software de rede que permite que muitos arquivos grandes sejam copiados e transportados para o {{site.data.keyword.cloud_notm}}.

<hr/>

## De que maneira os arquivos são armazenados no dispositivo de Mass Data Migration?
{: faq}

Os dispositivos Mass Data Migration usam um sistema de arquivos ZFS com compactação LZ4 e criptografia AES de 256 bits.

<hr/>

## Quanto custa para usar o Mass Data Migration nos EUA?
{: faq}

Nos EUA, uma taxa fixa de USD 395 é cobrada por dispositivo. Esse custo inclui a taxa do dispositivo de USD 295 e a Entrega aérea em um dia útil de roundtrip da UPS de USD 100, além de 10 dias úteis de uso em seu site.

<hr/>

## Quanto custa o uso do {{site.data.keyword.cos_full_notm}}?
{: faq}

A transferência de dados para o {{site.data.keyword.cloud_notm}} não tem nenhum custo para você. No entanto, as taxas padrão se aplicam a dados que estão armazenados no {{site.data.keyword.cos_full}} ou em qualquer outro serviço do {{site.data.keyword.cloud_notm}}. É possível localizar a precificação para o {{site.data.keyword.cos_full}} para a oferta Região cruzada padrão no link a seguir: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api ![Ícone de link externo](../../icons/launch-glyph.svg "Ícone de link externo")

<hr/>

## É possível comprar um dispositivo de Mass Data Migration do {{site.data.keyword.cloud_notm}}?
{: faq}

Os dispositivos {{site.data.keyword.cloud_notm}} Mass Data Migration não estão à venda.

<hr/>

## De que maneira o processo de Mass Data Migration do {{site.data.keyword.cloud_notm}} mantém a exclusividade dos nomes de objeto?
{: faq}

Para assegurar que os nomes de objeto sejam exclusivos quando eles forem copiados para o depósito, o caminho do arquivo será incluído como um prefixo no nome do objeto. Por exemplo, `/root/user/config.ini` torna-se `root/user/config.ini` quando copiado para o depósito.

## O que acontece se o depósito de destino não existir na conta do {{site.data.keyword.cos_full_notm}}?
{: faq}

Se o depósito de destino não existir, ele será criado. Se ele existir, deverá estar vazio,
caso contrário, a cópia não poderá continuar.  

## Os links são ignorados durante o processo de varredura?
{: faq}

Sim. Symlinks e links físicos são ignorados durante o processo de varredura.
