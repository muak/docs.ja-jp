---
title: 識別子名
description: C# プログラミング言語の有効な識別子名に関する規則について説明します。
ms.date: 08/21/2018
ms.openlocfilehash: e5ff83661c9a86273760f32a795f7de6dbc7bf1d
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/06/2018
ms.locfileid: "43877875"
---
# <a name="identifier-names"></a><span data-ttu-id="ad4c9-103">識別子名</span><span class="sxs-lookup"><span data-stu-id="ad4c9-103">Identifier names</span></span>

<span data-ttu-id="ad4c9-104">**識別子**は、型 (クラス、インターフェイス、構造体、デリゲート、列挙型)、メンバー、変数、名前空間に割り当てる名前です。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-104">An **identifier** is the name you assign to a type (class, interface, struct, delegate, or enum), member, variable, or namespace.</span></span> <span data-ttu-id="ad4c9-105">識別子を有効にするには次の規則に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-105">Valid identifiers must follow these rules:</span></span>

- <span data-ttu-id="ad4c9-106">識別子の名前は文字または `_` で始まらなければなりません。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-106">Identifiers must start with a letter, or `_`.</span></span>
- <span data-ttu-id="ad4c9-107">識別子には、Unicode 文字、10 進数文字、Unicode 接続文字、Unicode 結合文字、Unicode 書式設定文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-107">Identifiers may contain Unicode letter characters, decimal digit characters, Unicode connecting characters, Unicode combining characters, or Unicode formatting characters.</span></span> <span data-ttu-id="ad4c9-108">Unicode カテゴリの詳細については、[Unicode カテゴリ データベース](https://www.unicode.org/reports/tr44/)に関するページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-108">For more information on Unicode categories, see the [Unicode Category Database](https://www.unicode.org/reports/tr44/).</span></span>
<span data-ttu-id="ad4c9-109">識別子で `@` プレフィックスを使用することで、C# キーワードに一致する識別子を宣言できます。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-109">You can declare identifiers that match C# keywords by using the `@` prefix on the identifier.</span></span> <span data-ttu-id="ad4c9-110">`@` は識別子名の一部ではありません。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-110">The `@` is not part of the identifier name.</span></span> <span data-ttu-id="ad4c9-111">たとえば、`@if` の場合、`if` という名前の識別子が宣言されます。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-111">For example, `@if` declares an identifier named `if`.</span></span> <span data-ttu-id="ad4c9-112">このような[逐語的識別子](../../language-reference/tokens/verbatim.md)は主に、他の言語で宣言された識別子との相互運用性のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-112">These [verbatim identifiers](../../language-reference/tokens/verbatim.md) are primarily for interoperability with identifiers declared in other languages.</span></span>

<span data-ttu-id="ad4c9-113">有効な識別子の完全な定義は、[C# 言語仕様の「Identifiers」 (識別子) トピック](../../../../_csharplang/spec/lexical-structure.md#identifiers)にあります。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-113">For a complete definition of valid identifiers, see the [Identifiers topic in the C# Language Specification](../../../../_csharplang/spec/lexical-structure.md#identifiers).</span></span>

## <a name="naming-conventions"></a><span data-ttu-id="ad4c9-114">名前付け規則</span><span class="sxs-lookup"><span data-stu-id="ad4c9-114">Naming conventions</span></span>

<span data-ttu-id="ad4c9-115">規則に加え、.NET API 全体で使用されるさまざまな識別子[命名規則](../../../standard/design-guidelines/naming-guidelines.md)があります。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-115">In addition to the rules, there are a number of identifier [naming conventions](../../../standard/design-guidelines/naming-guidelines.md) used throughout the .NET APIs.</span></span> <span data-ttu-id="ad4c9-116">慣例により、C# プログラムでは、型名、名前空間、すべてのパブリック メンバーに `PascalCase` が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-116">By convention, C# programs use `PascalCase` for type names, namespaces, and all public members.</span></span> <span data-ttu-id="ad4c9-117">また、次の規則が一般的です。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-117">In addition, the following conventions are common:</span></span>

- <span data-ttu-id="ad4c9-118">インターフェイス名は大文字 `I` で始まります。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-118">Interface names start with a capital `I`.</span></span>
- <span data-ttu-id="ad4c9-119">属性型は `Attribute` という単語で終わります。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-119">Attribute types end with the word `Attribute`.</span></span>
- <span data-ttu-id="ad4c9-120">列挙型では、フラグ以外に単数名詞が使用され、フラグに複数名詞が使用されます。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-120">Enum types use a singular noun for non-flags, and a plural noun for flags.</span></span>
- <span data-ttu-id="ad4c9-121">識別子には、連続する 2 つの `_` 文字を含めないでください。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-121">Identifiers should not contain two consecutive `_` characters.</span></span> <span data-ttu-id="ad4c9-122">このような文字は、コンパイラで生成される識別子のために予約されています。</span><span class="sxs-lookup"><span data-stu-id="ad4c9-122">Those names are reserved for compiler generated identifiers.</span></span>

## <a name="c-language-specification"></a><span data-ttu-id="ad4c9-123">C# 言語仕様</span><span class="sxs-lookup"><span data-stu-id="ad4c9-123">C# Language Specification</span></span>

[!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a><span data-ttu-id="ad4c9-124">参照</span><span class="sxs-lookup"><span data-stu-id="ad4c9-124">See Also</span></span>

- [<span data-ttu-id="ad4c9-125">C# プログラミング ガイド</span><span class="sxs-lookup"><span data-stu-id="ad4c9-125">C# Programming Guide</span></span>](../index.md)
- [<span data-ttu-id="ad4c9-126">インサイド C# プログラム</span><span class="sxs-lookup"><span data-stu-id="ad4c9-126">Inside a C# Program</span></span>](../inside-a-program/index.md)
- [<span data-ttu-id="ad4c9-127">C# リファレンス</span><span class="sxs-lookup"><span data-stu-id="ad4c9-127">C# Reference</span></span>](../../language-reference/index.md)
- [<span data-ttu-id="ad4c9-128">クラス</span><span class="sxs-lookup"><span data-stu-id="ad4c9-128">Classes</span></span>](../classes-and-structs/classes.md)
- [<span data-ttu-id="ad4c9-129">構造体</span><span class="sxs-lookup"><span data-stu-id="ad4c9-129">Structs</span></span>](../classes-and-structs/structs.md)
- [<span data-ttu-id="ad4c9-130">名前空間</span><span class="sxs-lookup"><span data-stu-id="ad4c9-130">Namespaces</span></span>](../namespaces/index.md)
- [<span data-ttu-id="ad4c9-131">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="ad4c9-131">Interfaces</span></span>](../interfaces/index.md)
- [<span data-ttu-id="ad4c9-132">デリゲート</span><span class="sxs-lookup"><span data-stu-id="ad4c9-132">Delegates</span></span>](../delegates/index.md)