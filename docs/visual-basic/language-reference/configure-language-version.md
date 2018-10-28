---
title: Visual Basic の言語バージョンを選択します。
description: 特定のコンパイラ バージョンを使用して、構文検証を実行するコンパイラを構成します。
ms.date: 05/24/2018
ms.openlocfilehash: 7628b5a7c27f5b26171d42e44a58598ef3d5d49f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194723"
---
# <a name="select-the-visual-basic-language-version"></a><span data-ttu-id="08da8-103">Visual Basic の言語バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="08da8-103">Select the Visual Basic language version</span></span>

<span data-ttu-id="08da8-104">Visual Basic コンパイラは、最新のメジャー バージョンがリリースされた言語の既定値です。</span><span class="sxs-lookup"><span data-stu-id="08da8-104">The Visual Basic compiler defaults to the latest major version of the language that has been released.</span></span> <span data-ttu-id="08da8-105">言語の新しいポイント リリースを使用して、プロジェクトをコンパイルすることができます。</span><span class="sxs-lookup"><span data-stu-id="08da8-105">You may choose to compile any project using a new point release of the language.</span></span> <span data-ttu-id="08da8-106">言語の新しいバージョンを選択すると、プロジェクトで最新の言語機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="08da8-106">Choosing a newer version of the language enables your project to make use of the latest language features.</span></span> <span data-ttu-id="08da8-107">他のシナリオでは、古いバージョンの言語を使用する場合、プロジェクトがクリーンにコンパイルすることを検証する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08da8-107">In other scenarios, you may need to validate that a project compiles cleanly when using an older version of the language.</span></span>

<span data-ttu-id="08da8-108">この機能によって、開発環境に新しいバージョンの SDK とツールをインストールすることの決定と新しい言語機能をプロジェクトに組み込むことの決定が別になります。</span><span class="sxs-lookup"><span data-stu-id="08da8-108">This capability decouples the decision to install new versions of the SDK and tools in your development environment from the decision to incorporate new language features in a project.</span></span> <span data-ttu-id="08da8-109">ビルド コンピューターに最新の SDK とツールをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="08da8-109">You can install the latest SDK and tools on your build machine.</span></span> <span data-ttu-id="08da8-110">特定バージョンの言語をビルドに使用するように各プロジェクトを構成できます。</span><span class="sxs-lookup"><span data-stu-id="08da8-110">Each project can be configured to use a specific version of the language for its build.</span></span>

<span data-ttu-id="08da8-111">言語バージョンを設定する 3 つの方法はあります。</span><span class="sxs-lookup"><span data-stu-id="08da8-111">There are three ways to set the language version:</span></span>

- <span data-ttu-id="08da8-112">手動で編集、 [ **.vbproj**ファイル](#edit-the-vbproj-file)</span><span class="sxs-lookup"><span data-stu-id="08da8-112">Manually edit your [**.vbproj** file](#edit-the-vbproj-file)</span></span>
- <span data-ttu-id="08da8-113">言語バージョンを設定[サブディレクトリ内の複数のプロジェクト](#configure-multiple-projects)</span><span class="sxs-lookup"><span data-stu-id="08da8-113">Set the language version [for multiple projects in a subdirectory](#configure-multiple-projects)</span></span>
- <span data-ttu-id="08da8-114">構成、 [ `-langversion`コンパイラ オプション](#set-the-langversion-compiler-option)</span><span class="sxs-lookup"><span data-stu-id="08da8-114">Configure the [`-langversion` compiler option](#set-the-langversion-compiler-option)</span></span>

## <a name="edit-the-vbproj-file"></a><span data-ttu-id="08da8-115">Vbproj ファイルを編集します。</span><span class="sxs-lookup"><span data-stu-id="08da8-115">Edit the vbproj file</span></span>

<span data-ttu-id="08da8-116">言語バージョンを設定することができます、 **.vbproj**ファイル。</span><span class="sxs-lookup"><span data-stu-id="08da8-116">You can set the language version in your **.vbproj** file.</span></span> <span data-ttu-id="08da8-117">次の要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="08da8-117">Add the following element:</span></span>

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="08da8-118">値`latest`Visual Basic 言語の最新のマイナー バージョンを使用します。</span><span class="sxs-lookup"><span data-stu-id="08da8-118">The value `latest` uses the latest minor version of the Visual Basic language.</span></span> <span data-ttu-id="08da8-119">次の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="08da8-119">Valid values are:</span></span>

|<span data-ttu-id="08da8-120">[値]</span><span class="sxs-lookup"><span data-stu-id="08da8-120">Value</span></span>|<span data-ttu-id="08da8-121">説明</span><span class="sxs-lookup"><span data-stu-id="08da8-121">Meaning</span></span>|
|------------|-------------|
|<span data-ttu-id="08da8-122">default</span><span class="sxs-lookup"><span data-stu-id="08da8-122">default</span></span>|<span data-ttu-id="08da8-123">コンパイラは、最新のメジャー バージョンからサポートできるすべての有効な言語構文を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-123">The compiler accepts all valid language syntax from the latest major version that it can support.</span></span>|
|<span data-ttu-id="08da8-124">9</span><span class="sxs-lookup"><span data-stu-id="08da8-124">9</span></span>|<span data-ttu-id="08da8-125">コンパイラは、Visual Basic 9.0 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-125">The compiler accepts only syntax that is included in Visual Basic 9.0 or lower.</span></span>|
|<span data-ttu-id="08da8-126">10</span><span class="sxs-lookup"><span data-stu-id="08da8-126">10</span></span>|<span data-ttu-id="08da8-127">コンパイラは、Visual Basic 10.0 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-127">The compiler accepts only syntax that is included in Visual Basic 10.0 or lower.</span></span>|
|<span data-ttu-id="08da8-128">11</span><span class="sxs-lookup"><span data-stu-id="08da8-128">11</span></span>|<span data-ttu-id="08da8-129">コンパイラは、Visual Basic 11.0 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-129">The compiler accepts only syntax that is included in Visual Basic 11.0 or lower.</span></span>|
|<span data-ttu-id="08da8-130">12</span><span class="sxs-lookup"><span data-stu-id="08da8-130">12</span></span>|<span data-ttu-id="08da8-131">コンパイラは、Visual Basic 12.0 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-131">The compiler accepts only syntax that is included in Visual Basic 12.0 or lower.</span></span>|
|<span data-ttu-id="08da8-132">14</span><span class="sxs-lookup"><span data-stu-id="08da8-132">14</span></span>|<span data-ttu-id="08da8-133">コンパイラは、Visual Basic 14.0 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-133">The compiler accepts only syntax that is included in Visual Basic 14.0 or lower.</span></span>|
|<span data-ttu-id="08da8-134">16</span><span class="sxs-lookup"><span data-stu-id="08da8-134">15</span></span>|<span data-ttu-id="08da8-135">コンパイラは、Visual Basic 15.0 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-135">The compiler accepts only syntax that is included in Visual Basic 15.0 or lower.</span></span>|
|<span data-ttu-id="08da8-136">15.3</span><span class="sxs-lookup"><span data-stu-id="08da8-136">15.3</span></span>|<span data-ttu-id="08da8-137">コンパイラは、Visual Basic 15.3 の新機能に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-137">The compiler accepts only syntax that is included in Visual Basic 15.3 or lower.</span></span>|
|<span data-ttu-id="08da8-138">15.5</span><span class="sxs-lookup"><span data-stu-id="08da8-138">15.5</span></span>|<span data-ttu-id="08da8-139">コンパイラは、Visual Basic 15.5 に含まれている構文のみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-139">The compiler accepts only syntax that is included in Visual Basic 15.5 or lower.</span></span>|
|<span data-ttu-id="08da8-140">latest</span><span class="sxs-lookup"><span data-stu-id="08da8-140">latest</span></span>|<span data-ttu-id="08da8-141">コンパイラは、サポートできるすべての有効な言語の構文を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="08da8-141">The compiler accepts all valid language syntax that it can support.</span></span>|

<span data-ttu-id="08da8-142">特殊文字列の `default` と `latest` はそれぞれ、ビルド コンピューターにインストールされている最新のメジャー言語バージョンとマイナー言語バージョンに解決されます。</span><span class="sxs-lookup"><span data-stu-id="08da8-142">The special strings `default` and `latest` resolve to the latest major and minor language versions installed on the build machine, respectively.</span></span>

## <a name="configure-multiple-projects"></a><span data-ttu-id="08da8-143">複数のプロジェクトを構成する</span><span class="sxs-lookup"><span data-stu-id="08da8-143">Configure multiple projects</span></span>

<span data-ttu-id="08da8-144">複数のディレクトリを構成する `<LangVersion>` 要素を含む **Directory.build.props** ファイルを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="08da8-144">You can create a **Directory.build.props** file that contains the `<LangVersion>` element to configure multiple directories.</span></span> <span data-ttu-id="08da8-145">この操作は通常、ソリューション ディレクトリで実行します。</span><span class="sxs-lookup"><span data-stu-id="08da8-145">You typically do that in your solution directory.</span></span> <span data-ttu-id="08da8-146">ソリューション ディレクトリ内の **Directory.build.props** ファイルに以下を追加します。</span><span class="sxs-lookup"><span data-stu-id="08da8-146">Add the following to a **Directory.build.props** file in your solution directory:</span></span>

```xml
<Project>
 <PropertyGroup>
   <LangVersion>15.5</LangVersion>
 </PropertyGroup>
</Project>
```

<span data-ttu-id="08da8-147">ここで、そのファイルを含むディレクトリのすべてのサブディレクトリにビルドは Visual Basic バージョン 15.5 の構文を使用します。</span><span class="sxs-lookup"><span data-stu-id="08da8-147">Now, builds in every subdirectory of the directory containing that file will use Visual Basic version 15.5 syntax.</span></span> <span data-ttu-id="08da8-148">詳しくは、「[ビルドのカスタマイズ](/visualstudio/msbuild/customize-your-build.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08da8-148">For more information, see the article on [Customize your build](/visualstudio/msbuild/customize-your-build.md).</span></span>

## <a name="set-the-langversion-compiler-option"></a><span data-ttu-id="08da8-149">言語コンパイラ オプションを設定する</span><span class="sxs-lookup"><span data-stu-id="08da8-149">Set the langversion compiler option</span></span>

<span data-ttu-id="08da8-150">`-langversion` コマンド ライン オプションを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="08da8-150">You can use the `-langversion` command-line option.</span></span> <span data-ttu-id="08da8-151">詳しくは、[-langversion](../reference/command-line-compiler/langversion.md) コンパイラ オプションに関する記事を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08da8-151">For more information, see the article on the [-langversion](../reference/command-line-compiler/langversion.md) compiler option.</span></span> <span data-ttu-id="08da8-152">入力すると有効な値の一覧を表示できます`vbc -langversion:?`します。</span><span class="sxs-lookup"><span data-stu-id="08da8-152">You can see a list of the valid values by typing  `vbc -langversion:?` .</span></span>