---
title: 機械学習のタスク
description: ML.NET でサポートされる機械学習のさまざまなタスクについて説明します。
ms.date: 06/04/2018
author: aditidugar
ms.author: johalex
ms.openlocfilehash: 22249ac2d275a4168dbd8b03b90d9698fe90f2d1
ms.sourcegitcommit: d8bf4976eafe3289275be3811e7cb721bfff7e1e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2018
ms.locfileid: "34860698"
---
# <a name="machine-learning-tasks"></a><span data-ttu-id="f1555-103">機械学習のタスク</span><span class="sxs-lookup"><span data-stu-id="f1555-103">Machine learning tasks</span></span>

<span data-ttu-id="f1555-104">機械学習モデルを構築する場合は、データを使用して実現したい目的を最初に定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1555-104">When building a machine learning model, you first need to define what you are hoping to achieve with your data.</span></span> <span data-ttu-id="f1555-105">その後で、状況に適した機械学習のタスクを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f1555-105">After, you can pick the right machine learning task for your situation.</span></span> <span data-ttu-id="f1555-106">選択可能な機械学習のさまざまなタスクといくつかの一般的なユース ケースについて以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="f1555-106">The following list describes the different machine learning tasks that you can choose from and some common use cases.</span></span> 

> [!NOTE]
> <span data-ttu-id="f1555-107">ML.NET は現在プレビュー段階です。</span><span class="sxs-lookup"><span data-stu-id="f1555-107">ML.NET is currently in Preview.</span></span> <span data-ttu-id="f1555-108">現時点では、機械学習のタスクがすべてサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="f1555-108">Not all machine learning tasks are currently supported.</span></span> <span data-ttu-id="f1555-109">特定のタスクに対するご要望を送信するには、[dotnet/machinelearning リポジトリ](https://github.com/dotnet/machinelearning/issues)で問題をオープンしてください。</span><span class="sxs-lookup"><span data-stu-id="f1555-109">To submit a request for a certain task, open an issue in the [dotnet/machinelearning repository](https://github.com/dotnet/machinelearning/issues).</span></span>

> [!NOTE]
> <span data-ttu-id="f1555-110">現時点で、ML.NET は画像を使用する機械学習のタスクをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="f1555-110">Currently, ML.NET does not support machine learning tasks with images.</span></span> <span data-ttu-id="f1555-111">このサポートは今後のリリースで追加される予定です。</span><span class="sxs-lookup"><span data-stu-id="f1555-111">Support will be added in future releases.</span></span> 

## <a name="binary-classification"></a><span data-ttu-id="f1555-112">二項分類</span><span class="sxs-lookup"><span data-stu-id="f1555-112">Binary classification</span></span>

<span data-ttu-id="f1555-113">データのインスタンスが 2 つのうちのどちらのクラス (カテゴリ) に属しているかを予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="f1555-113">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict which of two classes (categories) an instance of data belongs to.</span></span> <span data-ttu-id="f1555-114">分類アルゴリズムの入力はラベル付けされた一連のサンプルであり、各ラベルは整数 0 または 1 です。</span><span class="sxs-lookup"><span data-stu-id="f1555-114">The input of a classification algorithm is a set of labeled examples, where each label is an integer of either 0 or 1.</span></span> <span data-ttu-id="f1555-115">二項分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1555-115">The output of a binary classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="f1555-116">二項分類のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f1555-116">Examples of binary classification scenarios include:</span></span>

* <span data-ttu-id="f1555-117">[Twitter コメントのセンチメントが "肯定的" か "否定的" かを理解する](../tutorials/sentiment-analysis.md)。</span><span class="sxs-lookup"><span data-stu-id="f1555-117">[Understanding sentiment of Twitter comments](../tutorials/sentiment-analysis.md) as either "positive" or "negative".</span></span>
* <span data-ttu-id="f1555-118">患者が特定の病気であるかどうかを診断する。</span><span class="sxs-lookup"><span data-stu-id="f1555-118">Diagnosing whether a patient has a certain disease or not.</span></span>
* <span data-ttu-id="f1555-119">電子メールを "スパム" としてマークするかどうかを決定する。</span><span class="sxs-lookup"><span data-stu-id="f1555-119">Making a decision to mark an email as "spam" or not.</span></span>

## <a name="multi-class-classification"></a><span data-ttu-id="f1555-120">多クラス分類</span><span class="sxs-lookup"><span data-stu-id="f1555-120">Multi-class classification</span></span>

<span data-ttu-id="f1555-121">データのインスタンスのクラス (カテゴリ) を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="f1555-121">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the class (category) of an instance of data.</span></span> <span data-ttu-id="f1555-122">分類アルゴリズムの入力は、ラベル付けされた一連のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="f1555-122">The input of a classification algorithm is a set of labeled examples.</span></span> <span data-ttu-id="f1555-123">各ラベルは 0 ～ k-1 の整数であり、k はクラスの数です。</span><span class="sxs-lookup"><span data-stu-id="f1555-123">Each label is an integer between 0 and k-1, where k is the number of classes.</span></span> <span data-ttu-id="f1555-124">分類アルゴリズムの出力は分類子であり、ラベルのない新しいインスタンスのクラスを予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1555-124">The output of a classification algorithm is a classifier, which you can use to predict the class of new unlabeled instances.</span></span> <span data-ttu-id="f1555-125">多クラス分類のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f1555-125">Examples of multi-class classification scenarios include:</span></span>

* <span data-ttu-id="f1555-126">"シベリアン ハスキー"、"ゴールデン レトリバー"、"プードル" などの犬種を特定する。</span><span class="sxs-lookup"><span data-stu-id="f1555-126">Determining the breed of a dog as a "Siberian Husky", "Golden Retriever", "Poodle", etc.</span></span>
* <span data-ttu-id="f1555-127">映画のレビューが "肯定的"、"中立"、"否定的" のどれかを理解する。</span><span class="sxs-lookup"><span data-stu-id="f1555-127">Understanding movie reviews as "positive", "neutral", or "negative".</span></span>
* <span data-ttu-id="f1555-128">ホテルのレビューを "立地"、"価格"、"清潔さ" などに分類する。</span><span class="sxs-lookup"><span data-stu-id="f1555-128">Categorizing hotel reviews as "location", "price", "cleanliness", etc.</span></span>

## <a name="regression"></a><span data-ttu-id="f1555-129">回帰</span><span class="sxs-lookup"><span data-stu-id="f1555-129">Regression</span></span>

<span data-ttu-id="f1555-130">関連する一連の特徴からラベルの値を予測するために使用する[教師あり機械学習](glossary.md#supervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="f1555-130">A [supervised machine learning](glossary.md#supervised-machine-learning) task that is used to predict the value of the label from a set of related features.</span></span> <span data-ttu-id="f1555-131">ラベルには任意の実際の値を使用できます。分類タスクのように有限の値のセットから取得するものではありません。</span><span class="sxs-lookup"><span data-stu-id="f1555-131">The label can be of any real value and is not from a finite set of values as in classification tasks.</span></span> <span data-ttu-id="f1555-132">回帰アルゴリズムでは、ラベルに関連する特徴におけるラベルの依存関係をモデル化して、特徴の値が変化するとラベルがどのように変化するかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f1555-132">Regression algorithms model the dependency of the label on its related features to determine how the label will change as the values of the features are varied.</span></span> <span data-ttu-id="f1555-133">回帰アルゴリズムの入力は、既知の値のラベルが付いた一連のサンプルです。</span><span class="sxs-lookup"><span data-stu-id="f1555-133">The input of a regression algorithm is a set of examples with labels of known values.</span></span> <span data-ttu-id="f1555-134">回帰アルゴリズムの出力は関数であり、新しい入力特徴のセットのラベル値を予測するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f1555-134">The output of a regression algorithm is a function, which you can use to predict the label value for any new set of input features.</span></span> <span data-ttu-id="f1555-135">回帰のシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f1555-135">Examples of regression scenarios include:</span></span>

* <span data-ttu-id="f1555-136">住宅の属性 (寝室数、立地、規模など) に基づいて住宅価格を予測する。</span><span class="sxs-lookup"><span data-stu-id="f1555-136">Predicting house prices based on house attributes such as number of bedrooms, location, or size.</span></span>
* <span data-ttu-id="f1555-137">履歴データと現在の市場動向に基づいて将来の株価を予測する。</span><span class="sxs-lookup"><span data-stu-id="f1555-137">Predicting future stock prices based on historical data and current market trends.</span></span>
* <span data-ttu-id="f1555-138">広告予算に基づいて製品の売り上げを予測する。</span><span class="sxs-lookup"><span data-stu-id="f1555-138">Predicting sales of a product based on advertising budgets.</span></span>

> [!NOTE]
> <span data-ttu-id="f1555-139">現在、ML.NET では時系列を含む回帰タスクのサポートを構築中です。</span><span class="sxs-lookup"><span data-stu-id="f1555-139">Currently, ML.NET is still building support for regression tasks that involve time series.</span></span>

## <a name="clustering"></a><span data-ttu-id="f1555-140">クラスタリング</span><span class="sxs-lookup"><span data-stu-id="f1555-140">Clustering</span></span>

<span data-ttu-id="f1555-141">データのインスタンスを、同様の特性を持つクラスタにグループ化するために使用する[教師なし機械学習](glossary.md#unsupervised-machine-learning)タスクです。</span><span class="sxs-lookup"><span data-stu-id="f1555-141">An [unsupervised machine learning](glossary.md#unsupervised-machine-learning) task that is used to group instances of data into clusters that contain similar characteristics.</span></span> <span data-ttu-id="f1555-142">また、閲覧や単純な観測では論理的に導き出せない可能性のあるデータ セットにおける関係をクラスタリングを使用して識別することもできます。</span><span class="sxs-lookup"><span data-stu-id="f1555-142">Clustering can also be used to identify relationships in a dataset that you might not logically derive by browsing or simple observation.</span></span> <span data-ttu-id="f1555-143">クラスタリング アルゴリズムの入力と出力は、選択した方法によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f1555-143">The inputs and outputs of a clustering algorithm depends on the methodology chosen.</span></span> <span data-ttu-id="f1555-144">分布、重心、結合性、または密度に基づくアプローチを利用できます。</span><span class="sxs-lookup"><span data-stu-id="f1555-144">You can take a distribution, centroid, connectivity, or density-based approach.</span></span> <span data-ttu-id="f1555-145">現在、ML.NET では、K 平均法によるクラスタリングを使用した重心に基づくアプローチをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f1555-145">ML.NET currently supports a centroid-based approach using K-Means clustering.</span></span> <span data-ttu-id="f1555-146">クラスタリングのシナリオの例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="f1555-146">Examples of clustering scenarios include:</span></span>

* <span data-ttu-id="f1555-147">ホテル選択の傾向と特性に基づいてホテルの宿泊客のセグメントを理解する。</span><span class="sxs-lookup"><span data-stu-id="f1555-147">Understanding segments of hotel guests based on habits and characteristics of hotel choices.</span></span>
* <span data-ttu-id="f1555-148">対象を絞った広告キャンペーンの構築に役立つ顧客セグメントと統計データを特定する。</span><span class="sxs-lookup"><span data-stu-id="f1555-148">Identifying customer segments and demographics to help build targeted advertising campaigns.</span></span>
* <span data-ttu-id="f1555-149">製造メトリックに基づいてインベントリを分類する。</span><span class="sxs-lookup"><span data-stu-id="f1555-149">Categorizing inventory based on manufacturing metrics.</span></span>

## <a name="anomaly-detection-coming-soon"></a><span data-ttu-id="f1555-150">異常検知 (*準備中*)</span><span class="sxs-lookup"><span data-stu-id="f1555-150">Anomaly detection (*coming soon*)</span></span>

## <a name="ranking-coming-soon"></a><span data-ttu-id="f1555-151">ランク付け (*準備中*)</span><span class="sxs-lookup"><span data-stu-id="f1555-151">Ranking (*coming soon*)</span></span>

## <a name="recommendation-coming-soon"></a><span data-ttu-id="f1555-152">推奨 (*準備中*)</span><span class="sxs-lookup"><span data-stu-id="f1555-152">Recommendation (*coming soon*)</span></span>
