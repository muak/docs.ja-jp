---
title: "ICorProfilerThreadEnum::Skip メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorProfilerThreadEnum.Skip
api_location: mscorwks.dll
api_type: COM
f1_keywords: ICorProfilerThreadEnum::Skip
helpviewer_keywords:
- Skip method, ICorProfilerThreadEnum interface [.NET Framework profiling]
- ICorProfilerThreadEnum::Skip method [.NET Framework profiling]
ms.assetid: acb8b029-4a96-4ed7-ae3c-310204e5ceea
topic_type: apiref
caps.latest.revision: "6"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: f492a455165f3b49994beb3220334e2932bf214c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="icorprofilerthreadenumskip-method"></a><span data-ttu-id="edb99-102">ICorProfilerThreadEnum::Skip メソッド</span><span class="sxs-lookup"><span data-stu-id="edb99-102">ICorProfilerThreadEnum::Skip Method</span></span>
<span data-ttu-id="edb99-103">指定した数の要素をスキップするため、この列挙子のカーソルを現在の位置から進めます。</span><span class="sxs-lookup"><span data-stu-id="edb99-103">Advances the enumerator's cursor from its current position to skip the specified number of elements.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="edb99-104">構文</span><span class="sxs-lookup"><span data-stu-id="edb99-104">Syntax</span></span>  
  
```  
HRESULT Skip (    [in] ULONG celt  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="edb99-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="edb99-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="edb99-106">[in]スキップする要素の数。</span><span class="sxs-lookup"><span data-stu-id="edb99-106">[in] The number of elements to be skipped.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="edb99-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="edb99-107">Return Value</span></span>  
 <span data-ttu-id="edb99-108">このメソッドは、次の特定の HRESULT と、メソッドの失敗を示す HRESULT エラーも返します。</span><span class="sxs-lookup"><span data-stu-id="edb99-108">This method returns the following specific HRESULTs as well as HRESULT errors that indicate method failure.</span></span>  
  
|<span data-ttu-id="edb99-109">HRESULT</span><span class="sxs-lookup"><span data-stu-id="edb99-109">HRESULT</span></span>|<span data-ttu-id="edb99-110">説明</span><span class="sxs-lookup"><span data-stu-id="edb99-110">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="edb99-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="edb99-111">S_OK</span></span>|<span data-ttu-id="edb99-112">`celt`要素がスキップされました。</span><span class="sxs-lookup"><span data-stu-id="edb99-112">`celt` elements were skipped.</span></span>|  
|<span data-ttu-id="edb99-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="edb99-113">S_FALSE</span></span>|<span data-ttu-id="edb99-114">少ない`celt`要素がスキップされた複数の要素ではありませんがあることを示します。</span><span class="sxs-lookup"><span data-stu-id="edb99-114">Fewer than `celt` elements were skipped, which indicates that there are no more elements.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="edb99-115">コメント</span><span class="sxs-lookup"><span data-stu-id="edb99-115">Remarks</span></span>  
 <span data-ttu-id="edb99-116">この列挙子のカーソルの新しい位置は、(現在の位置) +`celt`です。</span><span class="sxs-lookup"><span data-stu-id="edb99-116">The new position of this enumerator's cursor is (current position) + `celt`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="edb99-117">要件</span><span class="sxs-lookup"><span data-stu-id="edb99-117">Requirements</span></span>  
 <span data-ttu-id="edb99-118">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="edb99-118">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="edb99-119">**ヘッダー** : CorProf.idl、CorProf.h</span><span class="sxs-lookup"><span data-stu-id="edb99-119">**Header:** CorProf.idl, CorProf.h</span></span>  
  
 <span data-ttu-id="edb99-120">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="edb99-120">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="edb99-121">**.NET framework のバージョン:**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="edb99-121">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="edb99-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="edb99-122">See Also</span></span>  
 [<span data-ttu-id="edb99-123">ICorProfilerThreadEnum インターフェイス</span><span class="sxs-lookup"><span data-stu-id="edb99-123">ICorProfilerThreadEnum Interface</span></span>](../../../../docs/framework/unmanaged-api/profiling/icorprofilerthreadenum-interface.md)  
 [<span data-ttu-id="edb99-124">プロファイリングのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="edb99-124">Profiling Interfaces</span></span>](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)