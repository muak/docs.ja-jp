---
title: '&lt;issuerTokenResolver&gt;'
ms.date: 03/30/2017
ms.assetid: f74392f6-3f5b-4880-bd8a-3a9130d31e65
author: BrucePerlerMS
ms.openlocfilehash: eefd18c206b7f013c3a423df424c795583c0dde8
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216332"
---
# <a name="ltissuertokenresolvergt"></a>&lt;issuerTokenResolver&gt;
トークン ハンドラー コレクションのハンドラーによって使用される発行者トークン リゾルバーを登録します。 発行者トークン リゾルバーを使用して、受信トークンおよびメッセージの署名トークンを解決します。  
  
 \<system.identityModel>  
\<identityConfiguration>  
\<securityTokenHandlers>  
\<securityTokenHandlerConfiguration >  
\<issuerTokenResolver >  
  
## <a name="syntax"></a>構文  
  
```xml  
<system.identityModel>  
  <identityConfiguration>  
    <securityTokenHandlers>  
      <securityTokenHandlerConfiguration>  
        <issuerTokenResolver type=xs:string>  
        </issuerTokenResolver>  
      </securityTokenHandlerConfiguration>  
    </securityTokenHandlers>  
  </identityConfiguration>  
</system.identityModel>  
```  
  
## <a name="attributes-and-elements"></a>属性および要素  
 以降のセクションでは、属性、子要素、および親要素について説明します。  
  
### <a name="attributes"></a>属性  
  
|属性|説明|  
|---------------|-----------------|  
|型|発行者トークン リゾルバーの種類を指定します。 いずれかである必要があります、<xref:System.IdentityModel.Tokens.IssuerTokenResolver>クラスまたは型から派生した、<xref:System.IdentityModel.Tokens.IssuerTokenResolver>クラス。 必須。|  
  
### <a name="child-elements"></a>子要素  
 なし  
  
### <a name="parent-elements"></a>親要素  
  
|要素|説明|  
|-------------|-----------------|  
|[\<securityTokenHandlerConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/securitytokenhandlerconfiguration.md)|トークン ハンドラー コレクションのセキュリティの構成を提供します。|  
  
## <a name="remarks"></a>Remarks  
 発行者トークン リゾルバーを使用して、受信トークンおよびメッセージの署名トークンを解決します。 これを使用して、署名を確認するために使用される暗号化マテリアルを取得します。 指定する必要があります、`type`属性。 指定された型には、いずれかを指定できる<xref:System.IdentityModel.Tokens.IssuerTokenResolver>またはカスタム型から派生した、<xref:System.IdentityModel.Tokens.IssuerTokenResolver>クラス。  
  
 いくつかのトークン ハンドラーを使用すると、発行者トークン リゾルバーの設定を構成で指定できます。 セキュリティ トークン ハンドラー コレクションの指定された個々 のトークン ハンドラーの設定をオーバーライドします。  
  
> [!NOTE]
>  指定する、`<issuerTokenResolver>`要素の子要素として、 [ \<identityConfiguration >](../../../../../docs/framework/configure-apps/file-schema/windows-identity-foundation/identityconfiguration.md)要素は非推奨とされましたが、旧バージョンとの互換性もサポートします。 上の設定、`<securityTokenHandlerConfiguration>`要素のオーバーライド、`<identityConfiguration>`要素。  
  
## <a name="example"></a>例  
 次の XML から派生したカスタム クラスに基づいている発行者トークン リゾルバーの構成を表示する<xref:System.IdentityModel.Tokens.IssuerTokenResolver>します。 トークン リゾルバーは、カスタム構成要素から初期化された対象ユーザー キーのペアのディクショナリを保持 (`<AddAudienceKeyPair>`) クラスに対して定義されています。 クラスのオーバーライド、<xref:System.IdentityModel.Selectors.SecurityTokenResolver.LoadCustomConfiguration%2A>この要素を処理するメソッド。 次の例で、上書きを表示します。ただし、呼び出すメソッドは、簡潔にするためには表示されません。 完全な例では、次を参照してください。、`CustomToken`サンプル。  
  
```xml  
<issuerTokenResolver type="SimpleWebToken.CustomIssuerTokenResolver, SimpleWebToken">  
  <AddAudienceKeyPair  symmetricKey="wAVkldQiFypTQ+kdNdGWCYCHRcee8XmXxOvgmak8vSY=" audience="http://localhost:19851/" />  
</issuerTokenResolver>  
```  
  
## <a name="example"></a>例  
  
```  
public override void LoadCustomConfiguration(System.Xml.XmlNodeList nodelist)  
{  
    foreach (XmlNode node in nodelist)  
    {  
        XmlDictionaryReader rdr = XmlDictionaryReader.CreateDictionaryReader(new XmlTextReader(new StringReader(node.OuterXml)));  
        rdr.MoveToContent();  
  
        string symmetricKey = rdr.GetAttribute("symmetricKey");  
        string audience = rdr.GetAttribute("audience");  
  
        this.AddAudienceKeyPair(audience, symmetricKey);  
    }  
}  
```  
  
## <a name="see-also"></a>関連項目  
 <xref:System.IdentityModel.Tokens.IssuerTokenResolver>
