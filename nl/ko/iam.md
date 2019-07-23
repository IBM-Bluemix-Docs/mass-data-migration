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

# 사용자 액세스 권한
{: #manage-access}

{{site.data.keyword.mdms_full}}은 {{site.data.keyword.cloud_notm}} 콘솔에서 사용자를 관리하고 {{site.data.keyword.mdms_short}} 요청에 액세스할 수 있도록, {{site.data.keyword.iamlong}}에서 제어하는 중앙 집중식 액세스 제어 시스템을 지원합니다.
{: shortdesc}

이 기능은 {{site.data.keyword.mdms_short}} 베타 릴리스의 일부로 사용할 수 있습니다. 베타 프로그램 참여에 대한 자세한 정보는 [베타에 액세스하기](/docs/infrastructure/mass-data-migration?topic=mass-data-migration-releases#beta)를 확인하십시오.
{: note}

## 역할 및 권한
{: #roles}

계정 소유자는 {{site.data.keyword.cloud_notm}} 계정 내에서 정책을 설정하여 사용자별로 다른 액세스 레벨을 작성할 수 있습니다. {{site.data.keyword.mdms_short}} 요청을 작성한 후에는 {{site.data.keyword.cloud_notm}} 콘솔에서 주문의 진행상태를 추적할 수 있는 사용자를 결정하십시오. 

다음 표는 {{site.data.keyword.mdms_short}} 조치가 [{{site.data.keyword.cloud_notm}} IAM 플랫폼 관리 역할](/docs/iam?topic=iam-userroles#iamusermanrol)에 맵핑되는 방식을 보여줍니다.  

<table>
  <col width="20%">
  <col width="40%">
  <col width="40%">
  <tr>
    <th>플랫폼 관리 역할</th>
    <th>설명</th>
    <th>조치 예</th>
  </tr>
  <tr>
    <td><p>뷰어</p></td>
    <td><p>뷰어는 {{site.data.keyword.cloud_notm}} 계정 내에서 서비스 인스턴스에 대한 보기 전용 액세스 권한을 갖고 있습니다. 뷰어는 서비스 인스턴스를 작성하거나 수정할 수 없습니다. </p></td>
    <td>
      <p>
        <ul>
          <li>{{site.data.keyword.mdms_short}} 요청 세부사항 페이지 액세스</li>
          <li>{{site.data.keyword.mdms_short}} 주문 상태 보기</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>운영자</p></td>
    <td><p>운영자는 서비스 인스턴스를 보고, 별명, 바인딩 및 서비스 인증 정보를 관리할 수 있습니다. </p></td>
    <td>
      <p>
        <ul>
          <li>해당사항 없음</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>편집자</p></td>
    <td><p>편집자는 서비스 인스턴스 작성 및 삭제 권한을 포함하여 운영자 역할보다 많은 권한을 갖습니다. </p></td>
    <td>
      <p>
        <ul>
          <li>{{site.data.keyword.mdms_short}} 요청 작성</li>
        </ul>
      </p>
    </td>
  </tr>
  <tr>
    <td><p>관리자</p></td>
    <td><p>관리자는 새 사용자를 초대하고 다른 사용자에 대한 액세스 정책을 지정하는 권한을 포함하여 뷰어, 운영자 및 편집자가 수행할 수 있는 모든 조치를 수행할 수 있습니다. </p></td>
    <td>
      <p>
        <ul>
          <li>뷰어, 운영자 및 편집자가 수행할 수 있는 모든 조치</li>
          <li>사용자 액세스 정책 지정</li>
        </ul>
      </p>
    </td>
  </tr>
  <caption style="caption-side:bottom;">표 1. IAM(Identity and Access Management) 역할이 {{site.data.keyword.mdms_short}} 권한에 맵핑되는 방식 설명</caption>
</table>

UI에서 사용자 역할을 지정하는 방법에 대한 정보는 [리소스에 대한 액세스 관리](/docs/iam?topic=iam-iammanidaccser#iammanidaccser)를 참조하십시오.
{: tip}



