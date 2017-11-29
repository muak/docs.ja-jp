---
title: "ICorDebugProcessEnum::Next メソッド"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugProcessEnum.Next
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugProcessEnum::Next
helpviewer_keywords:
- Next method, ICorDebugProcessEnum interface [.NET Framework debugging]
- ICorDebugProcessEnum::Next method [.NET Framework debugging]
ms.assetid: 4ac7077c-8d88-49c4-b360-b3af0c541c63
topic_type: apiref
caps.latest.revision: "10"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 2628a6d2a93c66531acfbc20acff560f623854fd
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugprocessenumnext-method"></a><span data-ttu-id="24667-102">ICorDebugProcessEnum::Next メソッド</span><span class="sxs-lookup"><span data-stu-id="24667-102">ICorDebugProcessEnum::Next Method</span></span>
<span data-ttu-id="24667-103">列挙体の現在位置から ICorDebugProcess インスタンスの指定した数を取得します。</span><span class="sxs-lookup"><span data-stu-id="24667-103">Gets the specified number of ICorDebugProcess instances from the enumeration, starting at the current position.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="24667-104">構文</span><span class="sxs-lookup"><span data-stu-id="24667-104">Syntax</span></span>  
  
```  
HRESULT Next (  
    [in]  ULONG celt,  
    [out, size_is(celt), length_is(*pceltFetched)]  
        ICorDebugProcess *processes[],  
    [out] ULONG *pceltFetched  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="24667-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="24667-105">Parameters</span></span>  
 `celt`  
 <span data-ttu-id="24667-106">[in]数`ICorDebugProcess`を取得するインスタンス。</span><span class="sxs-lookup"><span data-stu-id="24667-106">[in] The number of `ICorDebugProcess` instances to be retrieved.</span></span>  
  
 `processess`  
 <span data-ttu-id="24667-107">[out]それぞれが指すポインターの配列、`ICorDebugProcess`プロセスを表すオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="24667-107">[out] An array of pointers, each of which points to an `ICorDebugProcess` object that represents a process.</span></span>  
  
 `pceltFetched`  
 <span data-ttu-id="24667-108">[out]数へのポインター`ICorDebugProcess`実際に返されるインスタンス。</span><span class="sxs-lookup"><span data-stu-id="24667-108">[out] Pointer to the number of `ICorDebugProcess` instances actually returned.</span></span> <span data-ttu-id="24667-109">この値を null にすることがある場合`celt`は 1 つです。</span><span class="sxs-lookup"><span data-stu-id="24667-109">This value may be null if `celt` is one.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="24667-110">要件</span><span class="sxs-lookup"><span data-stu-id="24667-110">Requirements</span></span>  
 <span data-ttu-id="24667-111">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="24667-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="24667-112">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="24667-112">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="24667-113">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="24667-113">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="24667-114">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="24667-114">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>