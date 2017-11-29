---
title: "IHostTaskManager::CreateTask メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostTaskManager.CreateTask
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostTaskManager::CreateTask
helpviewer_keywords:
- CreateTask method, IHostTaskManager interface [.NET Framework hosting]
- IHostTaskManager::CreateTask method [.NET Framework hosting]
ms.assetid: a6f8ad36-61e1-42b0-9db2-add575646d18
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c1ba71fcd35b16654ab67db3f657f7821c23b702
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="ihosttaskmanagercreatetask-method"></a><span data-ttu-id="c7389-102">IHostTaskManager::CreateTask メソッド</span><span class="sxs-lookup"><span data-stu-id="c7389-102">IHostTaskManager::CreateTask Method</span></span>
<span data-ttu-id="c7389-103">要求のホストが新しいタスクを作成することです。</span><span class="sxs-lookup"><span data-stu-id="c7389-103">Requests that the host create a new task.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c7389-104">構文</span><span class="sxs-lookup"><span data-stu-id="c7389-104">Syntax</span></span>  
  
```  
HRESULT CreateTask (  
    [in]  DWORD stacksize,   
    [in]  LPTHREAD_START_ROUTINE pStartAddress,  
    [in]  PVOID pParameter,  
    [out] IHostTask **ppTask  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="c7389-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c7389-105">Parameters</span></span>  
 `stacksize`  
 <span data-ttu-id="c7389-106">[in]要求されたサイズ、バイト単位の要求されたスタック、または既定のサイズを 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="c7389-106">[in] The requested size, in bytes, of the requested stack, or 0 (zero) for the default size.</span></span>  
  
 `pStartAddress`  
 <span data-ttu-id="c7389-107">[in]実行するタスクは、関数へのポインターです。</span><span class="sxs-lookup"><span data-stu-id="c7389-107">[in] A pointer to the function the task is to execute.</span></span>  
  
 `pParameter`  
 <span data-ttu-id="c7389-108">[in]関数は、関数、または null の場合に渡されるユーザー データへのポインターには、パラメーターはありません。</span><span class="sxs-lookup"><span data-stu-id="c7389-108">[in] A pointer to the user data to be passed to the function, or null if the function takes no parameters.</span></span>  
  
 `ppTask`  
 <span data-ttu-id="c7389-109">[out]アドレスへのポインター、 [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)タスクを作成できない場合に、ホスト、または null によって作成されたインスタンスです。</span><span class="sxs-lookup"><span data-stu-id="c7389-109">[out] A pointer to the address of an [IHostTask](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md) instance created by the host, or null if the task cannot be created.</span></span> <span data-ttu-id="c7389-110">呼び出しで明示的に開始されるまでに、タスクが中断されている状態のまま[ihosttask::start](../../../../docs/framework/unmanaged-api/hosting/ihosttask-start-method.md)です。</span><span class="sxs-lookup"><span data-stu-id="c7389-110">The task remains in a suspended state until it is explicitly started by a call to [IHostTask::Start](../../../../docs/framework/unmanaged-api/hosting/ihosttask-start-method.md).</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="c7389-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="c7389-111">Return Value</span></span>  
  
|<span data-ttu-id="c7389-112">HRESULT</span><span class="sxs-lookup"><span data-stu-id="c7389-112">HRESULT</span></span>|<span data-ttu-id="c7389-113">説明</span><span class="sxs-lookup"><span data-stu-id="c7389-113">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="c7389-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7389-114">S_OK</span></span>|<span data-ttu-id="c7389-115">`CreateTask`正常に返されます。</span><span class="sxs-lookup"><span data-stu-id="c7389-115">`CreateTask` returned successfully.</span></span>|  
|<span data-ttu-id="c7389-116">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="c7389-116">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="c7389-117">共通言語ランタイム (CLR) が、プロセスに読み込まれていませんまたは CLR は、状態をマネージ コードを実行またはできないの呼び出しは正常に処理します。</span><span class="sxs-lookup"><span data-stu-id="c7389-117">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="c7389-118">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="c7389-118">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="c7389-119">呼び出しがタイムアウトしました。</span><span class="sxs-lookup"><span data-stu-id="c7389-119">The call timed out.</span></span>|  
|<span data-ttu-id="c7389-120">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="c7389-120">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="c7389-121">呼び出し元は、ロックを所有していません。</span><span class="sxs-lookup"><span data-stu-id="c7389-121">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="c7389-122">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="c7389-122">HOST_E_ABANDONED</span></span>|<span data-ttu-id="c7389-123">イベントがキャンセルされましたブロックされたスレッドまたはファイバーが待機しています。</span><span class="sxs-lookup"><span data-stu-id="c7389-123">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="c7389-124">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="c7389-124">E_FAIL</span></span>|<span data-ttu-id="c7389-125">不明な致命的なエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="c7389-125">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="c7389-126">メソッドには、E_FAIL が返される、ときに、CLR は、プロセス内で使用可能ではなくなりました。</span><span class="sxs-lookup"><span data-stu-id="c7389-126">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="c7389-127">メソッドのホストに以降の呼び出しでは、HOST_E_CLRNOTAVAILABLE を返します。</span><span class="sxs-lookup"><span data-stu-id="c7389-127">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="c7389-128">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c7389-128">E_OUTOFMEMORY</span></span>|<span data-ttu-id="c7389-129">十分なメモリは、要求されたタスクを作成できませんでした。</span><span class="sxs-lookup"><span data-stu-id="c7389-129">Not enough memory was available to create the requested task.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c7389-130">コメント</span><span class="sxs-lookup"><span data-stu-id="c7389-130">Remarks</span></span>  
 <span data-ttu-id="c7389-131">CLR 呼び出し`CreateTask`をホストが新しいタスクを作成することを要求します。</span><span class="sxs-lookup"><span data-stu-id="c7389-131">The CLR calls `CreateTask` to request that the host create a new task.</span></span> <span data-ttu-id="c7389-132">ホストへのインターフェイス ポインターを返します、`IHostTask`インスタンス。</span><span class="sxs-lookup"><span data-stu-id="c7389-132">The host returns an interface pointer to an `IHostTask` instance.</span></span> <span data-ttu-id="c7389-133">返されたタスク必要があります中断したままへの呼び出しで明示的に開始されるまで`IHostTask::Start`です。</span><span class="sxs-lookup"><span data-stu-id="c7389-133">The returned task must remain suspended until it is explicitly started by a call to `IHostTask::Start`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c7389-134">要件</span><span class="sxs-lookup"><span data-stu-id="c7389-134">Requirements</span></span>  
 <span data-ttu-id="c7389-135">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="c7389-135">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c7389-136">**ヘッダー:** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="c7389-136">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="c7389-137">**ライブラリ:** MSCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="c7389-137">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="c7389-138">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c7389-138">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c7389-139">関連項目</span><span class="sxs-lookup"><span data-stu-id="c7389-139">See Also</span></span>  
 [<span data-ttu-id="c7389-140">ICLRTask インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c7389-140">ICLRTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtask-interface.md)  
 [<span data-ttu-id="c7389-141">ICLRTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c7389-141">ICLRTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrtaskmanager-interface.md)  
 [<span data-ttu-id="c7389-142">IHostTask インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c7389-142">IHostTask Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttask-interface.md)  
 [<span data-ttu-id="c7389-143">IHostTaskManager インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c7389-143">IHostTaskManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihosttaskmanager-interface.md)