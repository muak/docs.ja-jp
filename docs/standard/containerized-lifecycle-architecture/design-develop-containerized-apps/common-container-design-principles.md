---
title: "共通のコンテナー デザインの原則"
description: "Microsoft プラットフォームとツールが、Docker のコンテナー化アプリケーションのライフ サイクル"
keywords: "Docker, マイクロサービス, ASP.NET, コンテナー"
author: CESARDELATORRE
ms.author: wiwagn
ms.date: 09/22/2017
ms.openlocfilehash: d7186ae3b768384fe5c6b269578de8db5ef6064c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="common-container-design-principles"></a><span data-ttu-id="b6e3b-104">共通のコンテナー デザインの原則</span><span class="sxs-lookup"><span data-stu-id="b6e3b-104">Common container design principles</span></span>

<span data-ttu-id="b6e3b-105">事前に、開発プロセスを取得するはすコンテナーを使用する方法に関していくつかの基本的な概念です。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-105">Ahead of getting into the development process there are a few basic concepts worth mentioning with regard to how you use containers.</span></span>

## <a name="container-equals-a-process"></a><span data-ttu-id="b6e3b-106">コンテナーには、プロセスと等しい</span><span class="sxs-lookup"><span data-stu-id="b6e3b-106">Container equals a process</span></span>

<span data-ttu-id="b6e3b-107">コンテナー モデルでは、コンテナーは、1 つのプロセスを表します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-107">In the container model, a container represents a single process.</span></span> <span data-ttu-id="b6e3b-108">コンテナーを定義すると、プロセス境界として、スケール、またはバッチ オフ、プロセスに使用されるプリミティブの作成を開始します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-108">By defining a container as a process boundary, you begin to create the primitives used to scale, or batch-off, processes.</span></span> <span data-ttu-id="b6e3b-109">Docker コンテナーを実行すると表示されます、 [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint)定義します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-109">When you run a Docker container, you'll see an [ENTRYPOINT](https://docs.docker.com/engine/reference/builder/#/entrypoint) definition.</span></span> <span data-ttu-id="b6e3b-110">これは、プロセス、およびコンテナーの有効期間を定義します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-110">This defines the process and the lifetime of the container.</span></span> <span data-ttu-id="b6e3b-111">プロセスが完了したら、コンテナーのライフ サイクルが終了します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-111">When the process completes, the container life cycle ends.</span></span> <span data-ttu-id="b6e3b-112">Web サーバー、および Microsoft Azure として実装されていますが、バッチ ジョブなどの有効期間が短いプロセスなどの実行時間の長いプロセスが[WebJobs](https://azure.microsoft.com/en-us/documentation/articles/websites-webjobs-resources/)です。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-112">There are long-running processes, such as web servers, and short-lived processes, such as batch jobs, which might have been implemented as Microsoft Azure [WebJobs](https://azure.microsoft.com/en-us/documentation/articles/websites-webjobs-resources/).</span></span> <span data-ttu-id="b6e3b-113">プロセスが失敗した場合、コンテナーが終了し、Orchestrator が引き継ぎます。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-113">If the process fails, the container ends, and the orchestrator takes over.</span></span> <span data-ttu-id="b6e3b-114">Orchestrator が実行されている 5 つのインスタンスを保持するように指示しました、1 つが失敗した場合は、orchestrator は、失敗した処理を置換する別のコンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-114">If the orchestrator was instructed to keep five instances running and one fails, the orchestrator will create another container to replace the failed process.</span></span> <span data-ttu-id="b6e3b-115">バッチ ジョブで、プロセスはパラメーターを指定して開始されます。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-115">In a batch job, the process is started with parameters.</span></span> <span data-ttu-id="b6e3b-116">プロセスが完了すると、作業が完了します。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-116">When the process completes, the work is complete.</span></span>

<span data-ttu-id="b6e3b-117">複数のプロセスが 1 つのコンテナーで実行するシナリオがあります。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-117">You might find a scenario in which you want multiple processes running in a single container.</span></span> <span data-ttu-id="b6e3b-118">任意のアーキテクチャのドキュメントではありません、"never、"は常にも、「常にします」。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-118">In any architecture document, there's never a "never," nor is there always an "always."</span></span> <span data-ttu-id="b6e3b-119">複数のプロセスを必要とするシナリオで一般的なパターンでは、使用する[スーパーバイザー](http://supervisord.org/)です。</span><span class="sxs-lookup"><span data-stu-id="b6e3b-119">For scenarios requiring multiple processes, a common pattern is to use [Supervisor](http://supervisord.org/).</span></span>


>[!div class="step-by-step"]
<span data-ttu-id="b6e3b-120">[前](デザインの docker-applications.md) [次へ] (モノリシック applications.md)</span><span class="sxs-lookup"><span data-stu-id="b6e3b-120">[Previous] (design-docker-applications.md) [Next] (monolithic-applications.md)</span></span>