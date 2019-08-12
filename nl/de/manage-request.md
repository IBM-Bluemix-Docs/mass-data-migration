---

copyright:
  years:  2019
lastupdated: "2019-07-10"

keywords: submit order, create order, create request, submit request, track order, track request

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

# Anforderung verwalten
{: #manage-request}

Verwenden Sie das {{site.data.keyword.slportal}}, um Ihre {{site.data.keyword.mdms_full}}-Bestellung zu verwalten und ihren Status zu verfolgen.
{: shortdesc}

Wenn Sie am {{site.data.keyword.mdms_short}}-Betaprogramm teilnehmen, können Sie ein neues {{site.data.keyword.mdms_short}}-Service-Dashboard testen, auf das Sie von der {{site.data.keyword.cloud_notm}}-Konsole aus zugreifen können. Weitere Informationen finden Sie in [Am Betaprogramm teilnehmen](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-beta).
{: tip}

## Bestellung verfolgen 
{: #track-order}

Nachdem Sie eine Speichereinheit angefordert haben, können Sie den Fortschritt Ihrer Bestellung verfolgen, indem Sie die [{{site.data.keyword.mdms_short}}-Anforderungsdetailseite](https://control.softlayer.com/storage/mdms){: external} verwenden, die über das {{site.data.keyword.slportal}} verfügbar ist. 

In der folgenden Tabelle wird dargestellt, wie sich der Status der Bestellung ändert, wenn {{site.data.keyword.mdms_short}} die Anforderung verarbeitet. 

| Status | Beschreibung |
| --- | --- |
| Anforderung wird verarbeitet | Nachdem {{site.data.keyword.mdms_short}} die Anforderung empfangen hat, ändert sich der Status in _Anforderung wird verarbeitet_. |
| Einheit wird vorbereitet | Nachdem Ihre Bestellung genehmigt wurde, ändert sich der Anforderungsstatus in _Einheit wird vorbereitet_. {{site.data.keyword.mdms_short}} bereitet die nächste verfügbare Speichereinheit vor und konfiguriert sie. |
| Lieferung vorgesehen | Die vorkonfigurierte Speichereinheit wartet auf den Versand an Ihren Standort. Nachdem die Anforderung in den Status _Lieferung vorgesehen_ gewechselt ist, kann sie nicht mehr abgebrochen werden. |
| Einheit wurde versandt | Die Speichereinheit wird vom Versandunternehmen abgeholt und an Ihren Standort transportiert. Die Tracking-Nummer finden Sie im Abschnitt _Details der Bestellung_ auf der [-Anforderungsdetailseite](https://control.softlayer.com/storage/mdms){: external}. |
| Einheit erhalten | Nachdem die Einheit an {{site.data.keyword.cloud_notm}} zurückgegeben wurde, ändert sich der Status in _Einheit erhalten_. |
| Daten auslagern | Während des Datenübertragungsprozesses ändert sich der Anforderungsstatus in _Daten auslagern_. Die Einheit ist im {{site.data.keyword.cloud_notm}}-Rechenzentrum mit dem Netz verbunden und die Datenauslagerung wird automatisch gestartet. |
| Auslagern abgeschlossen | Wenn der Auslagerungsprozess abgeschlossen ist, ändert sich der Anforderungsstatus in _Auslagern abgeschlossen_. Ihre Daten sind jetzt in dem Cloud Object Storage-Ziel verfügbar, das Sie in der ursprünglichen Anforderung angegeben haben. |
| Löschen abgeschlossen | {{site.data.keyword.mdms_short}} löscht Daten permanent aus der Einheit. Dabei werden NIST-Standards für die Datenbereinigung angewendet. Nachdem der Prozess der Datenlöschung abgeschlossen ist, ändert sich der Status der Bestellung in _Löschen abgeschlossen_.
{: caption="Tabelle 1. Beschreibung des Workflows für den Status der {{site.data.keyword.mdms_short}}-Bestellung" caption-side="top"}
