---
title: ポインター比較 (C# プログラミング ガイド)
ms.date: 07/20/2015
helpviewer_keywords:
- pointers [C#], comparison
ms.assetid: fcafd514-7405-4deb-8490-cc58efda5495
ms.openlocfilehash: fa980c944159c477c333762ffad569332fba9402
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/07/2018
ms.locfileid: "44086640"
---
# <a name="pointer-comparison-c-programming-guide"></a>ポインター比較 (C# プログラミング ガイド)
次の演算子を適用して、任意の型のポインターを比較できます。  
  
 **==   !=   \<   >   \<=   >=**  
  
 比較演算子は、2 つのオペランドのアドレスを符号なし整数のように比較します。  
  
## <a name="example"></a>例  
 [!code-csharp[csProgGuidePointers#16](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_1.cs)]  
  
 [!code-csharp[csProgGuidePointers#17](../../../csharp/programming-guide/unsafe-code-pointers/codesnippet/CSharp/pointer-comparison_2.cs)]  
  
## <a name="sample-output"></a>出力例  
 `True`  
  
 `False`  
  
## <a name="see-also"></a>参照

- [C# プログラミング ガイド](../../../csharp/programming-guide/index.md)  
- [ポインター式](../../../csharp/programming-guide/unsafe-code-pointers/pointer-expressions.md)  
- [C# 演算子](../../../csharp/language-reference/operators/index.md)  
- [ポインターの操作](../../../csharp/programming-guide/unsafe-code-pointers/manipulating-pointers.md)  
- [ポインター型](../../../csharp/programming-guide/unsafe-code-pointers/pointer-types.md)  
- [型](../../../csharp/language-reference/keywords/types.md)  
- [unsafe](../../../csharp/language-reference/keywords/unsafe.md)  
- [fixed ステートメント](../../../csharp/language-reference/keywords/fixed-statement.md)  
- [stackalloc](../../../csharp/language-reference/keywords/stackalloc.md)
