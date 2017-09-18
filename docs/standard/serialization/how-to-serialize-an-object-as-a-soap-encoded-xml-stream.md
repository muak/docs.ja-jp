---
title: "方法 : オブジェクトを SOAP エンコード済み XML ストリームとしてシリアル化する"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
- C++
- jsharp
helpviewer_keywords:
- SOAP, XML serialization
- XML serialization, SOAP
- serialization, SOAP
ms.assetid: af406e0a-fa3a-46dd-a7ba-c80731eba3a0
caps.latest.revision: 6
author: Erikre
ms.author: erikre
manager: erikre
ms.translationtype: HT
ms.sourcegitcommit: 717bcb6f9f72a728d77e2847096ea558a9c50902
ms.openlocfilehash: 84bdce1e7a877425a38a980ba306d38573add227
ms.contentlocale: ja-jp
ms.lasthandoff: 08/21/2017

---
# <a name="how-to-serialize-an-object-as-a-soap-encoded-xml-stream"></a>方法 : オブジェクトを SOAP エンコード済み XML ストリームとしてシリアル化する
  
 SOAP メッセージは XML を使用して作成されるため、<xref:System.Xml.Serialization.XmlSerializer> クラスを使用してクラスをシリアル化し、エンコード済みの SOAP メッセージを生成できます。 生成される XML は、[W3C (World Wide Web Consortium) のドキュメント『Simple Object Access Protocol (SOAP) 1.1』のセクション 5](https://www.w3.org/TR/2000/NOTE-SOAP-20000508/#_Toc478383512) に準拠します。 SOAP メッセージを使用して通信を行う XML Web サービスを作成する場合、特殊な SOAP 属性のセットをクラスやクラスのメンバーに適用することで、生成される XML ストリームをカスタマイズできます。 属性の一覧については、「[Attributes That Control Encoded SOAP Serialization](../../../docs/standard/serialization/attributes-that-control-encoded-soap-serialization.md)」を参照してください。  
  
### <a name="to-serialize-an-object-as-a-soap-encoded-xml-stream"></a>オブジェクトを SOAP エンコード済み XML ストリームとしてシリアル化するには  
  
1.  [XML スキーマ定義ツール (Xsd.exe)](../../../docs/standard/serialization/xml-schema-definition-tool-xsd-exe.md) を使用して、クラスを作成します。  
  
2.  `System.Xml.Serialization` の特別な属性を 1 つ以上適用します。 「エンコード済み SOAP シリアル化を制御する属性」の一覧を参照してください。  
  
3.  新しい `XmlTypeMapping` を作成し、シリアル化されるクラスの型を使用して `SoapReflectionImporter` メソッドを呼び出して、`ImportTypeMapping` を作成します。  
  
     `ImportTypeMapping` クラスの `SoapReflectionImporter` メソッドを呼び出して `XmlTypeMapping` を作成するコード例を次に示します。  
  
    ```vb  
    ' Serializes a class named Group as a SOAP message.  
    Dim myTypeMapping As XmlTypeMapping =
        New SoapReflectionImporter().ImportTypeMapping(GetType(Group))  
    ```  
  
    ```csharp  
    // Serializes a class named Group as a SOAP message.  
    XmlTypeMapping myTypeMapping =
        new SoapReflectionImporter().ImportTypeMapping(typeof(Group));
    ```  
  
4.  `XmlSerializer` を `XmlTypeMapping` コンストラクターに渡して、<xref:System.Xml.Serialization.XmlSerializer.%23ctor%28System.Xml.Serialization.XmlTypeMapping%29> クラスのインスタンスを作成します。  
  
    ```vb  
    Dim mySerializer As XmlSerializer = New XmlSerializer(myTypeMapping)  
    ```  
  
    ```csharp  
    XmlSerializer mySerializer = new XmlSerializer(myTypeMapping);  
    ```  
  
5.  `Serialize` メソッドまたは `Deserialize` メソッドを呼び出します。  
  
## <a name="example"></a>例  
  
```vb  
' Serializes a class named Group as a SOAP message.  
Dim myTypeMapping As XmlTypeMapping =
    New SoapReflectionImporter().ImportTypeMapping(GetType(Group))
Dim mySerializer As XmlSerializer = New XmlSerializer(myTypeMapping)  
```  
  
```csharp  
// Serializes a class named Group as a SOAP message.  
XmlTypeMapping myTypeMapping =
    new SoapReflectionImporter().ImportTypeMapping(typeof(Group));
XmlSerializer mySerializer = new XmlSerializer(myTypeMapping);  
```  
  
## <a name="see-also"></a>関連項目  
 [XML シリアル化および SOAP シリアル化](../../../docs/standard/serialization/xml-and-soap-serialization.md)   
 [エンコード済み SOAP シリアル化を制御する属性](../../../docs/standard/serialization/attributes-that-control-encoded-soap-serialization.md)   
 [XML Web サービスを使用した XML シリアル化](../../../docs/standard/serialization/xml-serialization-with-xml-web-services.md)   
 [方法 : オブジェクトをシリアル化する](../../../docs/standard/serialization/how-to-serialize-an-object.md)   
 [方法 : オブジェクトを逆シリアル化する](../../../docs/standard/serialization/how-to-deserialize-an-object.md)   
 [方法 : SOAP エンコード済み XML シリアル化をオーバーライドする](../../../docs/standard/serialization/how-to-override-encoded-soap-xml-serialization.md)
