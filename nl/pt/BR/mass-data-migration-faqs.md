---

copyright:
  years: 2017, 2018
lastupdated: "2018-09-19"

---
{:new_window: target="_blank"}

# FAQs

## ** O que é o  {{site.data.keyword.cloud_notm}}  Mass Data Migration? **

O {{site.data.keyword.cloud}} Mass Data Migration é um serviço de transferência de dados físicos que acelera o movimento seguro de terabytes para petabytes de dados no {{site.data.keyword.cloud_notm}} usando dispositivos de armazenamento móvel reforçados e de capacidade utilizável de 120 TB.

<hr/>

## ** Como o Mass Data Migration é iniciado? **

Use o [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} para enviar sua solicitação. Quando sua solicitação é aprovada e processada, o próximo dispositivo ou os dispositivos disponíveis são configurados e enviados a você com base em suas informações de rede e remessa. Use o link a seguir para começar agora: https://control.softlayer.com/storage/mdms

<hr/>

## **Por que usar o Mass Data Migration?**

Os dispositivos Mass Data Migration estão equipados para serem executados em quase qualquer ambiente, de data centers e escritórios a locais remotos, armazéns e navios. O Mass Data Migration também será uma alternativa se as opções de transferência de dados via rede forem de custo proibitivo, muito lentas ou indisponíveis.

<hr/>

## **Qual é o máximo de dados que podem ser transferidos usando o Mass Data Migration?**

Praticamente não há nenhum limite para a quantia de dados que pode ser transferida, sejam alguns terabytes até petabytes. Cada dispositivo contém até 120 TB de capacidade utilizável no RAID-6, mas é possível usar múltiplos dispositivos para acomodar cargas de trabalho maiores. O maior objeto único é limitado a 10 TB.

<hr/>

## **Os múltiplos dispositivos podem ser usados para mover cargas de trabalho maiores que excedem 120 TB? Se sim, como? **

Use múltiplos dispositivos em paralelo ou em uma série para mover todos os dados em uma migração única ou use um único dispositivo em migrações iterativas. Por exemplo, transfira 1 PB de dados usando nove dispositivos em paralelo ou use um único dispositivo em nove migrações separadas.

<hr/>

## **Quanto tempo leva para transferir os dados?**

Desde o momento em que um cliente envia uma solicitação do Mass Data Migration até quando seus dados se tornam acessíveis no depósito do {{site.data.keyword.cos_full}}, o tempo de retorno pode ser apenas sete dias. O desempenho da transferência é afetado pelo número de arquivos a serem transferidos. A transferência de milhões de arquivos pequenos leva mais tempo do que a mesma quantia de dados contidos em poucos arquivos.

<hr/>

## **Por quanto tempo o dispositivo Mass Data Migration pode ser mantido?**

Um dispositivo pode ser mantido no site sem nenhum custo pelos primeiros 10 dias úteis. Esse prazo não inclui o dia em que seu dispositivo é enviado ou o dia em que você o recebe. Se mais tempo for necessário para concluir sua ingestão, será possível estender seu uso por US$ 30 por dia posteriormente (aplica-se a regiões dos EUA e da UE).

<hr/>

## **Quais interfaces de rede o Mass Data Migration suporta?**

Os dispositivos Mass Data Migration têm interfaces de rede de 10 Gbps com as portas de rede RJ45 (CAT6a) e SFP+ de cobre. O conversor de RJ45 para SFP+ está incluso. As interfaces de 10 Gbps têm o recurso de quadros gigantes ativado.

<hr/>

## **Qual é a opção de envio padrão do Mass Data Migration?**

O Mass Data Migration usa Entrega aérea em um dia útil de roundtrip da UPS para enviar todos os dispositivos. O custo é incluído em uma taxa fixa baixa US$ 395 por dispositivo. Os clientes não conseguem selecionar métodos de remessa alternativos atualmente.

<hr/>

## **Em quais regiões o Mass Data Migration está disponível?**

O Mass Data Migration está disponível somente nos Estados Unidos e na União Europeia. Todos os dados são migrados para o {{site.data.keyword.cos_full}} na Região Cruzada Padrão dos EUA ou nas camadas de Região Cruzada da UE do serviço. Os dispositivos não podem ser enviados de uma região e retornados para outra região.

<hr/>

## **Quanto custa importar dados para o {{site.data.keyword.cloud_notm}}?**

Nenhuma taxa é incorrida para dados que são transferidos para o {{site.data.keyword.cloud_notm}}.

<hr/>

## **O Mass Data Migration pode ser usado para exportar dados para fora do {{site.data.keyword.cloud_notm}}?**

O Mass Data Migration não suporta a exportação de dados fora do {{site.data.keyword.cloud_notm}} atualmente.

<hr/>

## **O Mass Data Migration criptografa os dados?**

O Mass Data Migration criptografa todos os dados com a criptografia AES de 256 bits e fornece uma senha forte para desbloquear o conjunto de armazenamentos. Toda a transferência de dados dentro do
{{site.data.keyword.IBM}} é feita sobre SSL.

<hr/>

## **Como o Mass Data Migration protege fisicamente os dados?**

Todos os dispositivos do Mass Data Migration são alojados em gabinetes resistentes e duráveis. Essas caixas são à prova d'água, à prova de choque e invioláveis para garantir a segurança de roundtrip do dispositivo e dos dados.

<hr/>

## **Como a solicitação pode ser rastreada em todo o processo de migração?**

Para rastrear o status de sua solicitação, consulte a seção de solicitações ativas na página do Mass Data Migration no [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. É possível conectar-se ao portal usando o link a seguir: https://control.softlayer.com/storage/mdms

<hr/>

## **Como os dados são apagados depois de terem sido transferidos para o {{site.data.keyword.cos_full_notm}}?**

Assim que a transferência de seus dados para o {{site.data.keyword.cos_full}} é concluída, o {{site.data.keyword.IBM}} inicia imediatamente uma limpeza de dados de nível DOD de quatro etapas para apagar permanentemente seus dados do dispositivo.

<hr/>

## ** Qual é a interface de arquivo? **

O dispositivo Mass Data Migration tem o recurso de compartilhamentos com o Network File System (NFS) e o Bloco de Mensagens do Servidor (SMB) ativado por padrão.

<hr/>

## **Como a interface de arquivo é usada?**

Primeiro, desbloqueie o conjunto de criptografia. Em seguida, monte o compartilhamento no servidor que contém os dados que você pretende migrar. Inicie a cópia de seus arquivos de dados para o compartilhamento.

<hr/>

## **Quais são os benefícios da interface de arquivo no Mass Data Migration?**

A interface de arquivo é baseada no arquivo maduro e no software de rede que permite que muitos arquivos grandes sejam copiados e transportados para o {{site.data.keyword.cloud_notm}}.

<hr/>

## **Como os arquivos são armazenados no dispositivo Mass Data Migration?**

Os dispositivos Mass Data Migration usam um sistema de arquivos ZFS com compactação LZ4 e criptografia AES de 256 bits.

<hr/>

## **Quanto custa para usar o Mass Data Migration nos EUA?**

Nos EUA, uma taxa fixa de USD 395 é cobrada por dispositivo. Esse custo inclui a taxa do dispositivo de USD 295 e a Entrega aérea em um dia útil de roundtrip da UPS de USD 100, além de 10 dias úteis de uso em seu site.

<hr/>

## ** Quanto custa o  {{site.data.keyword.cos_full_notm}}  uso? **

A transferência de dados para o {{site.data.keyword.cloud_notm}} não tem nenhum custo para você. No entanto, as taxas padrão se aplicam a dados que estão armazenados no {{site.data.keyword.cos_full}} ou em qualquer outro serviço do {{site.data.keyword.cloud_notm}}. A precificação para o {{site.data.keyword.cos_full}} para a oferta padrão para Várias regiões está disponível no link a seguir: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

<hr/>

## **Um dispositivo {{site.data.keyword.cloud_notm}} Mass Data Migration pode ser comprado?**

Os dispositivos {{site.data.keyword.cloud_notm}} Mass Data Migration não estão à venda.
