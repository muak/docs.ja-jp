---
title: "ICorProfilerCallback::ClassLoadStarted メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerCallback.ClassLoadStarted
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerCallback::ClassLoadStarted
helpviewer_keywords:
- ICorProfilerCallback::ClassLoadStarted method [.NET Framework profiling]
- ClassLoadStarted method [.NET Framework profiling]
ms.assetid: 9f728de8-45c2-45a5-ac4a-45660bd36ecf
topic_type: apiref
caps.latest.revision: "12"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 8f1622fdbbeb1f200f996e49c432600165a029aa
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icorprofilercallbackclassloadstarted-method"></a><span data-ttu-id="3d115-102">ICorProfilerCallback::ClassLoadStarted メソッド</span><span class="sxs-lookup"><span data-stu-id="3d115-102">ICorProfilerCallback::ClassLoadStarted Method</span></span>
<span data-ttu-id="3d115-103">クラスが読み込まれていることをプロファイラーに通知します。</span><span class="sxs-lookup"><span data-stu-id="3d115-103">Notifies the profiler that a class is being loaded.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="3d115-104">構文</span><span class="sxs-lookup"><span data-stu-id="3d115-104">Syntax</span></span>  
  
```  
HRESULT ClassLoadStarted(  
    [in] ClassID classId);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="3d115-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3d115-105">Parameters</span></span>  
 `classId`  
 <span data-ttu-id="3d115-106">[in]読み込まれているクラスを識別します。</span><span class="sxs-lookup"><span data-stu-id="3d115-106">[in] Identifies the class that is being loaded.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="3d115-107">コメント</span><span class="sxs-lookup"><span data-stu-id="3d115-107">Remarks</span></span>  
 <span data-ttu-id="3d115-108">値`classId`まで情報の要求に対して無効です、 [icorprofilercallback::classloadfinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md)メソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="3d115-108">The value of `classId` is not valid for an information request until the [ICorProfilerCallback::ClassLoadFinished](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-classloadfinished-method.md) method is called.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="3d115-109">要件</span><span class="sxs-lookup"><span data-stu-id="3d115-109">Requirements</span></span>  
 <span data-ttu-id="3d115-110">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="3d115-110">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="3d115-111">**ヘッダー** : CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="3d115-111">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="3d115-112">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="3d115-112">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="3d115-113">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="3d115-113">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d115-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d115-114">See Also</span></span>  
 [<span data-ttu-id="3d115-115">ICorProfilerCallback インターフェイス</span><span class="sxs-lookup"><span data-stu-id="3d115-115">ICorProfilerCallback Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilercallback-interface.md)