---
title: エンティティ型
ms.date: 03/30/2017
ms.assetid: a6dee9ab-9e4a-48f2-a169-3f79cc15821c
ms.openlocfilehash: c694f29d36988ea52aeca650cf2bba2c50c91e89
ms.sourcegitcommit: 11f11ca6cefe555972b3a5c99729d1a7523d8f50
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/03/2018
ms.locfileid: "32765322"
---
# <a name="entity-type"></a>エンティティ型
*エンティティ型*は Entity Data Model (EDM) でのデータの構造を記述するための基本的なビルド ブロックです。 概念モデルでのエンティティ型は、顧客や注文のように、トップレベル概念の構造を表します。 エンティティ型は、エンティティ型のインスタンスのテンプレートです。 各テンプレートには、次の情報が含まれています。  
  
-   一意の名前  (必須)   
  
-   [エンティティ キー](../../../../docs/framework/data/adonet/entity-key.md) 1 つまたは複数のプロパティで定義します。 (必須)   
  
-   データの形式で[プロパティ](../../../../docs/framework/data/adonet/property.md)です。 (省略可能)   
  
-   [ナビゲーション プロパティ](../../../../docs/framework/data/adonet/navigation-property.md)から 1 つのナビゲーションを可能にする[終了](../../../../docs/framework/data/adonet/association-end.md)の[アソシエーション](../../../../docs/framework/data/adonet/association-type.md)もう一方の end にします。 (オプション)。  
  
 アプリケーションでは、エンティティ型のインスタンスが特定のオブジェクト (特定の顧客や注文など) を表します。 エンティティ型の各インスタンスを一意にいる必要があります[エンティティ キー](../../../../docs/framework/data/adonet/entity-key.md)内で、[エンティティ セット](../../../../docs/framework/data/adonet/entity-set.md)です。  
  
 2 つのエンティティ型のインスタンスは、型が同じであり、エンティティ キーの値が等しい場合にのみ、等価のインスタンスと見なされます。  
  
## <a name="example"></a>例  
 下のダイアグラムは、`Book`、`Publisher`、および `Author` という 3 つのエンティティ型の概念モデルを示しています。  
  
 ![モデルの例](../../../../docs/framework/data/adonet/media/examplemodel.gif "ExampleModel")  
  
 各エンティティ型のエンティティ キーを構成するプロパティには、"(キー)" と示されています。  
  
 [ADO.NET Entity Framework](../../../../docs/framework/data/adonet/ef/index.md)概念スキーマ定義言語と呼ばれるドメイン固有言語 (DSL) を使用して ([CSDL](../../../../docs/framework/data/adonet/ef/language-reference/csdl-specification.md)) 概念モデルを定義します。 次の CSDL は、上のダイアグラムに示された `Book` エンティティ型を定義しています。  
  
 [!code-xml[EDM_Example_Model#EntityExample](../../../../samples/snippets/xml/VS_Snippets_Data/edm_example_model/xml/books.edmx#entityexample)]  
  
## <a name="see-also"></a>関連項目  
 [Entity Data Model キーの概念](../../../../docs/framework/data/adonet/entity-data-model-key-concepts.md)  
 [Entity Data Model](../../../../docs/framework/data/adonet/entity-data-model.md)  
 [facet](../../../../docs/framework/data/adonet/facet.md)
