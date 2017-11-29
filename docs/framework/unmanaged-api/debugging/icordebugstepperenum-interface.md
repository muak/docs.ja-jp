---
title: ICorDebugStepperEnum Interface1
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugStepperEnum
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugStepperEnum
helpviewer_keywords: ICorDebugStepperEnum interface [.NET Framework debugging]
ms.assetid: 988718c1-1a4a-40f2-a04c-7d67e5cfe1e2
topic_type: apiref
caps.latest.revision: "11"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: c0ef1888026a5df59916fe7decc2955760c934d8
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/18/2017
---
# <a name="icordebugstepperenum-interface1"></a><span data-ttu-id="c11a8-102">ICorDebugStepperEnum Interface1</span><span class="sxs-lookup"><span data-stu-id="c11a8-102">ICorDebugStepperEnum Interface1</span></span>
<span data-ttu-id="c11a8-103">ICorDebugEnum メソッドを実装して、ICorDebugStepper 配列を列挙します。</span><span class="sxs-lookup"><span data-stu-id="c11a8-103">Implements ICorDebugEnum methods, and enumerates ICorDebugStepper arrays.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="c11a8-104">メソッド</span><span class="sxs-lookup"><span data-stu-id="c11a8-104">Methods</span></span>  
  
|<span data-ttu-id="c11a8-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="c11a8-105">Method</span></span>|<span data-ttu-id="c11a8-106">説明</span><span class="sxs-lookup"><span data-stu-id="c11a8-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="c11a8-107">Next メソッド</span><span class="sxs-lookup"><span data-stu-id="c11a8-107">Next Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugstepperenum-next-method.md)|<span data-ttu-id="c11a8-108">指定した数を取得`ICorDebugStepper`列挙体の現在位置からのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="c11a8-108">Gets the specified number of `ICorDebugStepper` instances from the enumeration, starting at the current position.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="c11a8-109">コメント</span><span class="sxs-lookup"><span data-stu-id="c11a8-109">Remarks</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c11a8-110">このインターフェイスは、コンピューター間またはプロセス間でのリモート呼び出しをサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="c11a8-110">This interface does not support being called remotely, either cross-machine or cross-process.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="c11a8-111">要件</span><span class="sxs-lookup"><span data-stu-id="c11a8-111">Requirements</span></span>  
 <span data-ttu-id="c11a8-112">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="c11a8-112">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="c11a8-113">**ヘッダー:** CorDebug.idl、CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="c11a8-113">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="c11a8-114">**ライブラリ:** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="c11a8-114">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="c11a8-115">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="c11a8-115">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c11a8-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="c11a8-116">See Also</span></span>  
 [<span data-ttu-id="c11a8-117">デバッグのインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c11a8-117">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)