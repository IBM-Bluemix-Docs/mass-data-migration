---

copyright:
  years: 2017, 2018
lastupdated: "2018-05-17"

---
{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

# FAQs do {{site.data.keyword.cloud_notm}} Mass Data Migration

## Q1. O que é o {{site.data.keyword.cloud_notm}} Mass Data Migration? 
O {{site.data.keyword.cloud}} Mass Data Migration é um serviço de transferência física de dados que acelera a movimentação segura de terabytes a petabytes de dados para o {{site.data.keyword.cloud_notm}} usando dispositivos de armazenamento móveis resistentes de capacidade utilizável de 120 TB. 

## Q2. Como eu começo a usar o Mass Data Migration? 
Use o [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window} para enviar sua solicitação. Quando sua solicitação for aprovada e processada, os próximos dispositivos disponíveis serão pré-configurados e enviados para você com base em suas informações de rede e de remessa. Use o link a seguir para começar agora: https://control.softlayer.com/storage/mdms

## Q3. Quem deve usar o Mass Data Migration? 
Os dispositivos do Mass Data Migration estão equipados para executar em quase qualquer ambiente, desde data centers e escritórios até locais remotos, armazéns e embarcações. O Mass Data Migration também é uma alternativa quando há opções muito caras, lentas ou indisponíveis de
transferência de dados pela rede.  

## Q4. Qual é a quantia de dados que eu posso transferir usando o Mass Data Migration?
Praticamente não há nenhum limite para a quantia de dados que pode ser transferida, sejam alguns terabytes até petabytes. Cada dispositivo contém até 120 TB de capacidade utilizável no RAID-6, mas é possível usar múltiplos dispositivos para acomodar cargas de trabalho maiores.

## Q5. Como posso usar múltiplos dispositivos para mover cargas de trabalho maiores que excedem 120 TB? 
Use múltiplos dispositivos em paralelo ou em uma série para mover todos os dados em uma migração única ou use um único dispositivo em migrações iterativas. Por exemplo, transfira 1 PB de dados usando nove dispositivos em paralelo ou use um único dispositivo em nove migrações separadas.

## Q6. Quanto tempo leva para transferir meus dados? 
Desde o momento em que um cliente envia uma solicitação do Mass Data Migration até quando seus dados se tornam acessíveis no depósito do {{site.data.keyword.cos_full}}, o tempo de retorno pode ser apenas sete dias.

## Q7. Em quanto tempo posso ter um dispositivo Mass Data Migration?  
Um dispositivo pode ser mantido no local sem nenhum custo durante os primeiros 10 dias úteis. Isso não inclui o dia em que seu dispositivo é enviado ou o dia em que você o recebe. Se mais tempo for necessário para concluir sua ingestão, será possível estender seu uso por US$ 30 por dia posteriormente (aplica-se a regiões dos EUA e da UE). 

## Q8. Quais interfaces de rede o Mass Data Migration suporta?  
Os dispositivos do Mass Data Migration têm interfaces de rede de 10 Gbps com portas de rede de cobre para RJ45 (CAT6a) e SFP+ (com conversor de RJ45 para SFP+ incluído).

## Q9. Qual é a opção de envio padrão do Mass Data Migration? 
O Mass Data Migration usa Entrega aérea em um dia útil UPS para enviar todos os dispositivos. O custo é incluído em uma taxa fixa baixa US$ 395 por dispositivo. Os clientes não conseguem selecionar métodos de remessa alternativos atualmente.

## Q10. Em quais regiões o Mass Data Migration está disponível? 
O Mass Data Migration está disponível somente nos Estados Unidos e na União Europeia. Todos os dados são migrados para camadas de serviços do {{site.data.keyword.cos_full}} em Várias regiões dos EUA ou da União Europeia, respectivamente. Os dispositivos não podem ser enviados de uma região e retornados para outra região.

## Q11. Qual o valor para importar dados para o {{site.data.keyword.cloud_notm}}? 
Não há taxas aplicáveis para dados transferidos para o {{site.data.keyword.cloud_notm}}.

## Q12: posso usar o Mass Data Migration para exportar meus dados para fora do
{{site.data.keyword.cloud_notm}}? 
O Mass Data Migration não suporta a exportação de dados fora do {{site.data.keyword.cloud_notm}} atualmente.

## Q13. O Mass Data Migration criptografa meus dados? 
O Mass Data Migration criptografa todos os dados com a criptografia AES de 256 bits e fornece uma senha forte para desbloquear o conjunto de armazenamentos. Toda a transferência de dados dentro do
{{site.data.keyword.IBM}} é feita sobre SSL.

## Q14. Como o Mass Data Migration protege meus dados fisicamente? 
Todos os dispositivos do Mass Data Migration são alojados em gabinetes resistentes e duráveis. Essas caixas são à prova d'água, à prova de choque e invioláveis para assegurar o roundtrip do dispositivo e a segurança de dados. 

## Q15. Como posso rastrear minha solicitação durante o processo de migração? 
Para rastrear o status de sua solicitação, consulte a seção de solicitações ativas na página do Mass Data Migration no [{{site.data.keyword.slportal}}](https://control.softlayer.com/){:new_window}. É possível conectar-se ao portal usando o link a seguir: https://control.softlayer.com/storage/mdms

## Q16. Como os meus dados são apagados do dispositivo depois que ele é transferido para o {{site.data.keyword.cos_full_notm}}?
Assim que a transferência de seus dados para o {{site.data.keyword.cos_full}} é concluída, o {{site.data.keyword.IBM}} inicia imediatamente uma limpeza de dados de nível DOD de quatro etapas para apagar permanentemente seus dados do dispositivo. 

## Q17: qual é a interface de arquivo no Mass Data Migration? 
O Mass Data Migration usa o Network File System (NFS).

## Q18: como a interface de arquivo é usada no Mass Data Migration? 
Depois de ter desbloqueado o conjunto de criptografia, monte o compartilhamento NFS no servidor que contém os dados que você pretende migrar e, em seguida, comece copiando seus arquivos de dados para o compartilhamento do NFS.

## Q19: quais são os benefícios da interface de arquivo no Mass Data Migration? 
A interface arquivo é baseada no arquivo maduro e no software de rede permitindo que grandes números de arquivos maiores sejam copiados e transportados para o {{site.data.keyword.cloud_notm}}.

## Q20: como os arquivos são armazenados no dispositivo Mass Data Migration? 
Os dispositivos Mass Data Migration usam um sistema de arquivos ZFS com compactação LZ4 e criptografia AES de 256 bits.

## Q21. Quanto custa para usar o Mass Data Migration nos EUA? 
Nos EUA, uma taxa fixa de US$ 395 é cobrada por dispositivo, incluindo a taxa de dispositivo de US$ 295, US$ 100 para Entrega aérea em um dia útil UPS e 10 dias úteis de uso em seu site. 

## Q22. Sou cobrado para uso do {{site.data.keyword.cos_full_notm}}? 
A transferência de dados no {{site.data.keyword.cloud_notm}} não incorre em nenhum custo para você, no entanto, taxas padrão serão aplicadas para dados armazenados no {{site.data.keyword.cos_full}} ou para qualquer outro serviço do {{site.data.keyword.cloud_notm}}. A precificação para o {{site.data.keyword.cos_full}} para a oferta padrão para Várias regiões está disponível no link a seguir: https://www.ibm.com/cloud-computing/bluemix/pricing-object-storage#s3api

## Q23. Posso comprar um dispositivo {{site.data.keyword.cloud_notm}} Mass Data Migration? 
Os dispositivos {{site.data.keyword.cloud_notm}} Mass Data Migration não estão disponíveis para compra. 
