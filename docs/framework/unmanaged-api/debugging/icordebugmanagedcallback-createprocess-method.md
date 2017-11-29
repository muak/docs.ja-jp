---
title: "ICorDebugManagedCallback::CreateProcess メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugManagedCallback.CreateProcess
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugManagedCallback::CreateProcess
helpviewer_keywords:
- ICorDebugManagedCallback::CreateProcess method [.NET Framework debugging]
- CreateProcess method, ICorDebugManagedCallback interface [.NET Framework debugging]
ms.assetid: 8e89d5ee-e4e3-4738-8302-0b7d1cf4846e
topic_type: apiref
caps.latest.revision: "13"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: bef3140717ff977fbfae813d0de89011b89ed062
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugmanagedcallbackcreateprocess-method"></a><span data-ttu-id="f60ca-102">ICorDebugManagedCallback::CreateProcess メソッド</span><span class="sxs-lookup"><span data-stu-id="f60ca-102">ICorDebugManagedCallback::CreateProcess Method</span></span>
<span data-ttu-id="f60ca-103">デバッガーは、プロセスをアタッチまたは、最初に起動されたときに通知します。</span><span class="sxs-lookup"><span data-stu-id="f60ca-103">Notifies the debugger when a process has been attached or started for the first time.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="f60ca-104">構文</span><span class="sxs-lookup"><span data-stu-id="f60ca-104">Syntax</span></span>  
  
```  
HRESULT CreateProcess (  
    [in] ICorDebugProcess *pProcess  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f60ca-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f60ca-105">Parameters</span></span>  
 `pProcess`  
 <span data-ttu-id="f60ca-106">[in]ICorDebugProcess を表すオブジェクトをアタッチまたは開始されたプロセスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f60ca-106">[in] A pointer to an ICorDebugProcess object that represents the process that has been attached or started.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f60ca-107">コメント</span><span class="sxs-lookup"><span data-stu-id="f60ca-107">Remarks</span></span>  
 <span data-ttu-id="f60ca-108">共通言語ランタイムが初期化されるまで、このメソッドは呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="f60ca-108">This method is not called until the common language runtime is initialized.</span></span> <span data-ttu-id="f60ca-109">ほとんどの[ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md)メソッドでは、前に CORDBG_E_NOTREADY を返します、`CreateProcess`コールバック。</span><span class="sxs-lookup"><span data-stu-id="f60ca-109">Most of the [ICorDebug](../../../../docs/framework/unmanaged-api/debugging/icordebug-interface.md) methods will return CORDBG_E_NOTREADY before the `CreateProcess` callback.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="f60ca-110">要件</span><span class="sxs-lookup"><span data-stu-id="f60ca-110">Requirements</span></span>  
 <span data-ttu-id="f60ca-111">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="f60ca-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="f60ca-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="f60ca-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="f60ca-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="f60ca-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="f60ca-114">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="f60ca-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f60ca-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f60ca-115">See Also</span></span>  
 [<span data-ttu-id="f60ca-116">ICorDebugManagedCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f60ca-116">ICorDebugManagedCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)