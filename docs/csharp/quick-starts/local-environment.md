---
title: "クイック スタート - ローカル環境 - C# ガイド"
description: "このクイック スタートでは、クイック スタートをローカルで実行するための基本について説明します。"
author: billwagner
ms.author: wiwagn
ms.date: 12/07/2017
ms.topic: article
ms.prod: .net
ms.technology: devlang-csharp
ms.devlang: csharp
ms.custom: mvc
ms.openlocfilehash: 4cbe66df4173854870dd6ac68c52e8c87c46c1f6
ms.sourcegitcommit: 9bee08539b1886c9d57fa3d5bd8a58dfdd7cad94
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/12/2017
---
# <a name="local-environment"></a><span data-ttu-id="de12a-103">ローカル環境</span><span class="sxs-lookup"><span data-stu-id="de12a-103">Local environment</span></span>

<span data-ttu-id="de12a-104">クイック スタートをローカルで実行するための最初の手順は、ローカル コンピューター上に開発環境をセットアップすることです。</span><span class="sxs-lookup"><span data-stu-id="de12a-104">The first step to trying a quick start locally is to setup a development environment on your local machine.</span></span>
<span data-ttu-id="de12a-105">Mac、PC、または Linux 上でローカルの開発環境を設定する手順については、.NET の [10 分でわかる概要](https://www.microsoft.com/net/core)に関するトピックに記載されています。</span><span class="sxs-lookup"><span data-stu-id="de12a-105">The .NET topic [Get Started in 10 minutes](https://www.microsoft.com/net/core) has instructions for setting up your local development environment on Mac, PC or Linux.</span></span>

<span data-ttu-id="de12a-106">または、[.NET Core SDK](http://dot.net/core) と [Visual Studio Code](https://code.visualstudio.com/) をインストールすることもできます。</span><span class="sxs-lookup"><span data-stu-id="de12a-106">Alternatively, you can install the [.NET Core SDK](http://dot.net/core) and [Visual Studio Code](https://code.visualstudio.com/).</span></span>

## <a name="basic-application-development-flow"></a><span data-ttu-id="de12a-107">アプリケーション開発の基本フロー</span><span class="sxs-lookup"><span data-stu-id="de12a-107">Basic application development flow</span></span>

<span data-ttu-id="de12a-108">[`dotnet new`](../../core/tools/dotnet-new.md) コマンドを使用してアプリケーションを作成します。</span><span class="sxs-lookup"><span data-stu-id="de12a-108">You'll create applications using the [`dotnet new`](../../core/tools/dotnet-new.md) command.</span></span> <span data-ttu-id="de12a-109">このコマンドによってアプリケーションに必要なファイルとアセットが生成されます。</span><span class="sxs-lookup"><span data-stu-id="de12a-109">This command generates the files and assets necessary for your application.</span></span> <span data-ttu-id="de12a-110">クイック スタートではすべて `console` タイプのアプリケーションを使用します。</span><span class="sxs-lookup"><span data-stu-id="de12a-110">The quickstarts all use the `console` application type.</span></span>

<span data-ttu-id="de12a-111">その他には、実行可能ファイルをビルドする [`dotnet build`](../../core/tools/dotnet-build.md) コマンド、実行可能ファイルを実行する [`dotnet run`](../../core/tools/dotnet-run.md) コマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="de12a-111">The other commands you'll use are [`dotnet build`](../../core/tools/dotnet-build.md) to build the executable, and [`dotnet run`](../../core/tools/dotnet-run.md) to run the executable.</span></span>

## <a name="pick-your-quickstart"></a><span data-ttu-id="de12a-112">クイック スタートを選択する</span><span class="sxs-lookup"><span data-stu-id="de12a-112">Pick your quickstart</span></span>

<span data-ttu-id="de12a-113">次のどのクイック スタートからでも始められます。</span><span class="sxs-lookup"><span data-stu-id="de12a-113">You can start with any of the following quick starts:</span></span>

## <a name="numbers-in-cnumbers-in-csharp-localmd"></a>[<span data-ttu-id="de12a-114">C# における数値</span><span class="sxs-lookup"><span data-stu-id="de12a-114">Numbers in C#</span></span>](numbers-in-csharp-local.md)

<span data-ttu-id="de12a-115">「[C# における数値](numbers-in-csharp-local.md)」クイック スタートでは、コンピューターが数値を格納する方法と、異なる数値型で計算を実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="de12a-115">In the [Numbers in C#](numbers-in-csharp-local.md) quick start, you'll learn how computers store numbers and how to perform calculations with different numeric types.</span></span> <span data-ttu-id="de12a-116">丸め処理の基礎と、C# で算術演算を実行する方法を学習します。</span><span class="sxs-lookup"><span data-stu-id="de12a-116">You'll learn the basics of rounding, and how to perform mathematical calculations using C#.</span></span> 

<span data-ttu-id="de12a-117">このクイック スタートでは、「[Hello World](hello-world.yml)」チュートリアルが終了していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="de12a-117">This quick start assumes that you have finished the [Hello world](hello-world.yml) tutorial.</span></span>

## <a name="branches-and-loopsbranches-and-loops-localmd"></a>[<span data-ttu-id="de12a-118">分岐とループ</span><span class="sxs-lookup"><span data-stu-id="de12a-118">Branches and loops</span></span>](branches-and-loops-local.md)

<span data-ttu-id="de12a-119">「[分岐とループ](branches-and-loops-local.md)」クイック スタートでは、変数に格納された値に基づいて、コード実行のさまざまなパスを選択する作業の基礎について説明します。</span><span class="sxs-lookup"><span data-stu-id="de12a-119">The [Branches and loops](branches-and-loops-local.md) quick start teaches the basics of selecting different paths of code execution based on the values stored in variables.</span></span> <span data-ttu-id="de12a-120">プログラムが決定して異なる操作を選択する上で基本となる、制御フローの基礎を学習します。</span><span class="sxs-lookup"><span data-stu-id="de12a-120">You'll learn the basics of control flow, which is the basis of how programs make decisions and choose different actions.</span></span> 

<span data-ttu-id="de12a-121">この入門レッスンでは、「[Hello World](hello-world.yml)」および「[C# における数値](numbers-in-csharp-local.md)」の各レッスンが終了していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="de12a-121">This beginning lesson assumes that you have finished the [Hello World](hello-world.yml) and [Numbers in C#](numbers-in-csharp-local.md) lessons.</span></span>

## <a name="list-collectionarrays-and-collectionsmd"></a>[<span data-ttu-id="de12a-122">リスト コレクション</span><span class="sxs-lookup"><span data-stu-id="de12a-122">List collection</span></span>](arrays-and-collections.md)

<span data-ttu-id="de12a-123">「[リスト コレクション](arrays-and-collections.md)」レッスンでは、データのシーケンスを格納するリスト コレクション型について説明します。</span><span class="sxs-lookup"><span data-stu-id="de12a-123">The [List collection](arrays-and-collections.md) lesson gives you a tour of the List collection type that stores sequences of data.</span></span> <span data-ttu-id="de12a-124">項目の追加方法や削除方法、項目の検索方法、リストを並べ替える方法を学習します。</span><span class="sxs-lookup"><span data-stu-id="de12a-124">You'll learn how to add and remove items, search for items, and sort the lists.</span></span> <span data-ttu-id="de12a-125">さまざまな種類のリストを紹介します。</span><span class="sxs-lookup"><span data-stu-id="de12a-125">You'll explore different kinds of lists.</span></span> 

<span data-ttu-id="de12a-126">この入門クイック スタートでは、上記のクイック スタートが終了していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="de12a-126">This beginning quick start assumes that you have finished the quick starts listed above.</span></span>

## <a name="introduction-to-classesintroduction-to-classesmd"></a>[<span data-ttu-id="de12a-127">クラスの概要</span><span class="sxs-lookup"><span data-stu-id="de12a-127">Introduction to classes</span></span>](introduction-to-classes.md)

<span data-ttu-id="de12a-128">この最後のクイック スタートは、お使いのマシンで、独自のローカルの開発環境と .NET Core を使用して行うためにのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="de12a-128">This final quickstart is only available to run on your machine, using your own local development environment and .NET Core.</span></span>
<span data-ttu-id="de12a-129">コンソール アプリケーションを構築し、C# 言語に含まれるオブジェクト指向の基本的な機能について学習します。</span><span class="sxs-lookup"><span data-stu-id="de12a-129">You'll build a console application and see the basic object-oriented features that are part of the C# language.</span></span>