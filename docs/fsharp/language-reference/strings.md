---
title: "文字列 (F#)"
description: "F# 'string' 型が変更できないテキストを Unicode 文字のシーケンスとして表現する方法について説明します。"
keywords: "visual f#, f#, 関数型プログラミング"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: df7624e5-ca6c-4e77-9e2b-87ca7e5e6f52
ms.openlocfilehash: 96a398ebcd53681481b10d1a2bee5f1e5442a5cd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="strings"></a><span data-ttu-id="a74bf-104">文字列</span><span class="sxs-lookup"><span data-stu-id="a74bf-104">Strings</span></span>

> [!NOTE]
<span data-ttu-id="a74bf-105">この記事の API リファレンスのリンクをクリックすると MSDN に移動します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-105">The API reference links in this article will take you to MSDN.</span></span>  <span data-ttu-id="a74bf-106">docs.microsoft.com API リファレンスは完全ではありません。</span><span class="sxs-lookup"><span data-stu-id="a74bf-106">The docs.microsoft.com API reference is not complete.</span></span>

<span data-ttu-id="a74bf-107">`string`型は、変更できないテキストを Unicode 文字のシーケンスとして表現します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-107">The `string` type represents immutable text as a sequence of Unicode characters.</span></span> <span data-ttu-id="a74bf-108">`string` は、.NET Framework の `System.String` のエイリアスです。</span><span class="sxs-lookup"><span data-stu-id="a74bf-108">`string` is an alias for `System.String` in the .NET Framework.</span></span>

## <a name="remarks"></a><span data-ttu-id="a74bf-109">コメント</span><span class="sxs-lookup"><span data-stu-id="a74bf-109">Remarks</span></span>
<span data-ttu-id="a74bf-110">文字列リテラルは引用符 (") 文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-110">String literals are delimited by the quotation mark (") character.</span></span> <span data-ttu-id="a74bf-111">円記号 (\)特定の特殊文字をエンコードするために使用します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-111">The backslash character (\) is used to encode certain special characters.</span></span> <span data-ttu-id="a74bf-112">円記号と、次の文字の組み合わせと呼ばれる、*エスケープ シーケンス*です。</span><span class="sxs-lookup"><span data-stu-id="a74bf-112">The backslash and the next character together are known as an *escape sequence*.</span></span> <span data-ttu-id="a74bf-113">サポートされるエスケープ シーケンス f# 文字列リテラルは、次の表に表示されます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-113">Escape sequences supported in F# string literals are shown in the following table.</span></span>

|<span data-ttu-id="a74bf-114">文字</span><span class="sxs-lookup"><span data-stu-id="a74bf-114">Character</span></span>|<span data-ttu-id="a74bf-115">エスケープ シーケンス</span><span class="sxs-lookup"><span data-stu-id="a74bf-115">Escape sequence</span></span>|
|---------|---------------|
|<span data-ttu-id="a74bf-116">バックスペース</span><span class="sxs-lookup"><span data-stu-id="a74bf-116">Backspace</span></span>|<span data-ttu-id="a74bf-117">\b</span><span class="sxs-lookup"><span data-stu-id="a74bf-117">\b</span></span>|
|<span data-ttu-id="a74bf-118">改行</span><span class="sxs-lookup"><span data-stu-id="a74bf-118">Newline</span></span>|\n|
|<span data-ttu-id="a74bf-119">キャリッジ リターン</span><span class="sxs-lookup"><span data-stu-id="a74bf-119">Carriage return</span></span>|<span data-ttu-id="a74bf-120">\r</span><span class="sxs-lookup"><span data-stu-id="a74bf-120">\r</span></span>|
|<span data-ttu-id="a74bf-121">タブ</span><span class="sxs-lookup"><span data-stu-id="a74bf-121">Tab</span></span>|<span data-ttu-id="a74bf-122">\t</span><span class="sxs-lookup"><span data-stu-id="a74bf-122">\t</span></span>|
|<span data-ttu-id="a74bf-123">円記号</span><span class="sxs-lookup"><span data-stu-id="a74bf-123">Backslash</span></span>|\\|
|<span data-ttu-id="a74bf-124">引用符</span><span class="sxs-lookup"><span data-stu-id="a74bf-124">Quotation mark</span></span>|\"|
|<span data-ttu-id="a74bf-125">アポストロフィ</span><span class="sxs-lookup"><span data-stu-id="a74bf-125">Apostrophe</span></span>|\'|
|<span data-ttu-id="a74bf-126">Unicode 文字</span><span class="sxs-lookup"><span data-stu-id="a74bf-126">Unicode character</span></span>|<span data-ttu-id="a74bf-127">\u*XXXX*または \U*XXXXXXXX* (ここで*X* 16 進数の数字を示します)</span><span class="sxs-lookup"><span data-stu-id="a74bf-127">\u*XXXX* or \U*XXXXXXXX* (where *X* indicates a hexadecimal digit)</span></span>|

<span data-ttu-id="a74bf-128">前にある場合、@ 記号、リテラルは、逐語的文字列。</span><span class="sxs-lookup"><span data-stu-id="a74bf-128">If preceded by the @ symbol, the literal is a verbatim string.</span></span> <span data-ttu-id="a74bf-129">つまり、2 つの引用符文字が 1 つの引用符の文字として解釈されることを除き、エスケープ シーケンスを無視することです。</span><span class="sxs-lookup"><span data-stu-id="a74bf-129">This means that any escape sequences are ignored, except that two quotation mark characters are interpreted as one quotation mark character.</span></span>

<span data-ttu-id="a74bf-130">さらに、文字列は、三重引用符で囲むことがあります。</span><span class="sxs-lookup"><span data-stu-id="a74bf-130">Additionally, a string may be enclosed by triple quotes.</span></span> <span data-ttu-id="a74bf-131">この場合、すべてのエスケープ シーケンスは無視されます、二重引用符文字も含まれます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-131">In this case, all escape sequences are ignored, including double quotation mark characters.</span></span> <span data-ttu-id="a74bf-132">含む埋め込み文字列を引用符で囲まれた文字列を指定するには、逐語的文字列または三重引用符で囲まれた文字列か、使用できます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-132">To specify a string that contains an embedded quoted string, you can either use a verbatim string or a triple-quoted string.</span></span> <span data-ttu-id="a74bf-133">逐語的文字列を使用する場合は、単一引用符文字を示すために 2 つの引用符文字を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a74bf-133">If you use a verbatim string, you  must specify two quotation mark characters to indicate a single quotation mark character.</span></span> <span data-ttu-id="a74bf-134">三重引用符で囲まれた文字列を使用する場合は、文字列の末尾として解析されることがなく、単一引用符文字を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-134">If you use a triple-quoted string, you can use the single quotation mark characters without them being parsed as the end of the string.</span></span> <span data-ttu-id="a74bf-135">この手法は、XML または埋め込まれた引用符を含むその他の構造を使用するときに役に立ちます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-135">This technique can be useful when you work with XML or other structures that include embedded quotation marks.</span></span>

```fsharp
// Using a verbatim string
let xmlFragment1 = @"<book author=""Milton, John"" title=""Paradise Lost"">"

// Using a triple-quoted string
let xmlFragment2 = """<book author="Milton, John" title="Paradise Lost">"""
```

<span data-ttu-id="a74bf-136">コードでは、文字列は、改行が受け入れられ、改行として解釈されます、改行文字として、円記号が改行の前に、最後の文字でない限り。</span><span class="sxs-lookup"><span data-stu-id="a74bf-136">In code, strings that have line breaks are accepted and the line breaks are interpreted literally as newlines, unless a backslash character is the last character before the line break.</span></span> <span data-ttu-id="a74bf-137">次の行の先頭の空白文字には、バック スラッシュ文字を使用する場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-137">Leading whitespace on the next line is ignored when the backslash character is used.</span></span> <span data-ttu-id="a74bf-138">次のコードは、文字列を生成`str1`値を持つ`"abc\n     def"`および文字列`str2`値を持つ`"abcdef"`します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-138">The following code produces a string `str1` that has value `"abc\n     def"` and a string `str2` that has value `"abcdef"`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1001.fs)]

<span data-ttu-id="a74bf-139">文字列内の個々 の文字は、次のように配列に似た構文を使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-139">You can access individual characters in a string by using array-like syntax, as follows.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1002.fs)]

<span data-ttu-id="a74bf-140">出力は `b`になります。</span><span class="sxs-lookup"><span data-stu-id="a74bf-140">The output is `b`.</span></span>

<span data-ttu-id="a74bf-141">または、次のコードに示すように、配列スライス構文を使用して部分文字列を抽出することができます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-141">Or you can extract substrings by using array slice syntax, as shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1003.fs)]

<span data-ttu-id="a74bf-142">出力は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="a74bf-142">The output is as follows.</span></span>

```
abc
def
```

<span data-ttu-id="a74bf-143">型の符号なしバイトの配列で ASCII 文字列を表すことができる`byte[]`です。</span><span class="sxs-lookup"><span data-stu-id="a74bf-143">You can represent ASCII strings by arrays of unsigned bytes, type `byte[]`.</span></span> <span data-ttu-id="a74bf-144">サフィックスを追加する`B`を ASCII 文字列であることを示すリテラル文字列。</span><span class="sxs-lookup"><span data-stu-id="a74bf-144">You add the suffix `B` to a string literal to indicate that it is an ASCII string.</span></span> <span data-ttu-id="a74bf-145">ASCII 文字列リテラルがバイト配列を使用では、Unicode のエスケープ シーケンスを除くの Unicode 文字列として同じエスケープ シーケンスをサポートします。</span><span class="sxs-lookup"><span data-stu-id="a74bf-145">ASCII string literals used with byte arrays support the same escape sequences as Unicode strings, except for the Unicode escape sequences.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1004.fs)]
    
## <a name="string-operators"></a><span data-ttu-id="a74bf-146">文字列演算子</span><span class="sxs-lookup"><span data-stu-id="a74bf-146">String Operators</span></span>
<span data-ttu-id="a74bf-147">文字列を連結する 2 つの方法があります: を使用して、`+`演算子またはを使用して、`^`演算子。</span><span class="sxs-lookup"><span data-stu-id="a74bf-147">There are two ways to concatenate strings: by using the `+` operator or by using the `^` operator.</span></span> <span data-ttu-id="a74bf-148">`+`演算子は、機能を処理する .NET Framework の文字列との互換性を維持します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-148">The `+` operator maintains compatibility with the .NET Framework string handling features.</span></span>

<span data-ttu-id="a74bf-149">次の例は、文字列の連結を示しています。</span><span class="sxs-lookup"><span data-stu-id="a74bf-149">The following example illustrates string concatenation.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1006.fs)]
    
## <a name="string-class"></a><span data-ttu-id="a74bf-150">String クラス</span><span class="sxs-lookup"><span data-stu-id="a74bf-150">String Class</span></span>
<span data-ttu-id="a74bf-151">F# の文字列型は .NET Framework では実際にため`System.String`すべての入力、`System.String`メンバーは、使用します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-151">Because the string type in F# is actually a .NET Framework `System.String` type, all the `System.String` members are available.</span></span> <span data-ttu-id="a74bf-152">これが含まれています、`+`演算子を使用する場合は、文字列を連結する、`Length`プロパティ、および`Chars`プロパティで、文字列を Unicode 文字の配列として返します。</span><span class="sxs-lookup"><span data-stu-id="a74bf-152">This includes the `+` operator, which is used to concatenate strings, the `Length` property, and the `Chars` property, which returns the string as an array of Unicode characters.</span></span> <span data-ttu-id="a74bf-153">文字列の詳細については、次を参照してください。`System.String`です。</span><span class="sxs-lookup"><span data-stu-id="a74bf-153">For more information about strings, see `System.String`.</span></span>

<span data-ttu-id="a74bf-154">使用して、`Chars`プロパティ`System.String`文字列内の個々 の文字は、次のコードに示すように、インデックスを指定することによってアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a74bf-154">By using the `Chars` property of `System.String`, you can access the individual characters in a string by specifying an index, as is shown in the following code.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-1/snippet1005.fs)]
    
## <a name="string-module"></a><span data-ttu-id="a74bf-155">String モジュール</span><span class="sxs-lookup"><span data-stu-id="a74bf-155">String Module</span></span>
<span data-ttu-id="a74bf-156">文字列を処理するための追加機能が含まれる、`String`内のモジュール、`FSharp.Core`名前空間。</span><span class="sxs-lookup"><span data-stu-id="a74bf-156">Additional functionality for string handling is included in the `String` module in the `FSharp.Core` namespace.</span></span> <span data-ttu-id="a74bf-157">詳細については、次を参照してください。 [Core.String モジュール](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.string-module-%5bfsharp%5d)です。</span><span class="sxs-lookup"><span data-stu-id="a74bf-157">For more information, see [Core.String Module](https://msdn.microsoft.com/visualfsharpdocs/conceptual/core.string-module-%5bfsharp%5d).</span></span>

## <a name="see-also"></a><span data-ttu-id="a74bf-158">関連項目</span><span class="sxs-lookup"><span data-stu-id="a74bf-158">See Also</span></span>
[<span data-ttu-id="a74bf-159">F# 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="a74bf-159">F# Language Reference</span></span>](index.md)