---
title: "IAppDomainBinding インターフェイス"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IAppDomainBinding
api_location: mscoree.dll
api_type: COM
f1_keywords: IAppDomainBinding
helpviewer_keywords: IAppDomainBinding interface [.NET Framework hosting]
ms.assetid: 368881ab-c4ea-4731-bf22-c596aac7c66c
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2e02c1b9499bc2972f88c9045d3f59423edb6cb2
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="iappdomainbinding-interface"></a><span data-ttu-id="97496-102">IAppDomainBinding インターフェイス</span><span class="sxs-lookup"><span data-stu-id="97496-102">IAppDomainBinding Interface</span></span>
<span data-ttu-id="97496-103">共通言語ランタイム (CLR) にホスト アプリケーションにアプリケーション ドメインが作成されていることを通知で呼び出されるメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="97496-103">Provides a method that is called by the common language runtime (CLR) to notify the host application that an application domain has been created.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="97496-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="97496-104">Methods</span></span>  
  
|<span data-ttu-id="97496-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="97496-105">Method</span></span>|<span data-ttu-id="97496-106">説明</span><span class="sxs-lookup"><span data-stu-id="97496-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="97496-107">OnAppDomain メソッド</span><span class="sxs-lookup"><span data-stu-id="97496-107">OnAppDomain Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iappdomainbinding-onappdomain-method.md)|<span data-ttu-id="97496-108">共通言語ランタイム (CLR) にアプリケーション ドメインが作成されているホストに通知によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="97496-108">Called by the common language runtime (CLR) to notify the host that an application domain has been created.</span></span>|  
  
## <a name="requirements"></a><span data-ttu-id="97496-109">要件</span><span class="sxs-lookup"><span data-stu-id="97496-109">Requirements</span></span>  
 <span data-ttu-id="97496-110">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="97496-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="97496-111">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="97496-111">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="97496-112">**ライブラリ:** MSCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="97496-112">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="97496-113">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="97496-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="97496-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="97496-114">See Also</span></span>  
 [<span data-ttu-id="97496-115">ホスト インターフェイス</span><span class="sxs-lookup"><span data-stu-id="97496-115">Hosting Interfaces</span></span>](../../../../docs/framework/unmanaged-api/hosting/hosting-interfaces.md)