---
title: "GetTypeLibInfo 関数"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetTypeLibInfo
api_location: TlbRef.dll
api_type: DLLExport
f1_keywords: GetTypeLibInfo
helpviewer_keywords: GetTypeLibInfo function [.NET Framework]
ms.assetid: a1c4d165-9bdc-4ca8-940e-292d4ffcc338
topic_type: apiref
caps.latest.revision: "16"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: a5dc55a9538798b81dce9db02583c271b9f2ed54
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="gettypelibinfo-function"></a><span data-ttu-id="92177-102">GetTypeLibInfo 関数</span><span class="sxs-lookup"><span data-stu-id="92177-102">GetTypeLibInfo Function</span></span>
<span data-ttu-id="92177-103">確認するには、指定したタイプ ライブラリに関する情報を返します、 [TLIBATTR](https://msdn.microsoft.com/library/ms221376\(v=vs.85\).aspx)構造体。</span><span class="sxs-lookup"><span data-stu-id="92177-103">Returns information about the specified type library by examining its [TLIBATTR](https://msdn.microsoft.com/library/ms221376\(v=vs.85\).aspx) structure.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="92177-104">構文</span><span class="sxs-lookup"><span data-stu-id="92177-104">Syntax</span></span>  
  
```  
HRESULT GetTypeLibInfo(  
    [in]   LPWSTR     szFile,  
    [out]  GUID      *pTypeLibID,  
    [out]  LCID      *pTypeLibLCID,  
    [out]  SYSKIND   *pTypeLibPlatform,  
    [out]  USHORT    *pTypeLibMajorVer,  
    [out]  USHORT    *pTypeLibMinorVer  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="92177-105">パラメーター</span><span class="sxs-lookup"><span data-stu-id="92177-105">Parameters</span></span>  
 `szFile`  
 <span data-ttu-id="92177-106">[in]タイプ ライブラリのファイル名。</span><span class="sxs-lookup"><span data-stu-id="92177-106">[in] The file name of the type library.</span></span>  
  
 `pTypeLibID`  
 <span data-ttu-id="92177-107">[out]タイプ ライブラリの GUID です。</span><span class="sxs-lookup"><span data-stu-id="92177-107">[out] The GUID of the type library.</span></span>  
  
 `pTypeLibLCID`  
 <span data-ttu-id="92177-108">[out]タイプ ライブラリのローカリゼーション ID です。</span><span class="sxs-lookup"><span data-stu-id="92177-108">[out] The localization ID of the type library.</span></span>  
  
 `pTypeLibPlatform`  
 <span data-ttu-id="92177-109">[out]A [SYSKIND](https://msdn.microsoft.com/library/ms221272\(v=vs.85\).aspx)をタイプ ライブラリのターゲットのオペレーティング システムを識別するフラグ。</span><span class="sxs-lookup"><span data-stu-id="92177-109">[out] A [SYSKIND](https://msdn.microsoft.com/library/ms221272\(v=vs.85\).aspx) flag that identifies the target operating system for the type library.</span></span> <span data-ttu-id="92177-110">一般的な値は、SYS_WIN32 SYS_WIN64 です。</span><span class="sxs-lookup"><span data-stu-id="92177-110">Common values are SYS_WIN32 and SYS_WIN64.</span></span>  
  
 `pTypeLibMajorVer`  
 <span data-ttu-id="92177-111">[out]タイプ ライブラリのメジャー バージョン番号。</span><span class="sxs-lookup"><span data-stu-id="92177-111">[out] The major version number of the type library.</span></span> <span data-ttu-id="92177-112">たとえば、バージョン*x.y*、メジャー バージョン番号は*x*です。</span><span class="sxs-lookup"><span data-stu-id="92177-112">For example, for version *x.y*, the major version number is *x*.</span></span>  
  
 `pTypeLibMinorVer`  
 <span data-ttu-id="92177-113">[out]タイプ ライブラリのマイナー バージョン番号。</span><span class="sxs-lookup"><span data-stu-id="92177-113">[out] The minor version number of the type library.</span></span> <span data-ttu-id="92177-114">たとえば、バージョン*x.y*、マイナー バージョン番号は*y*です。</span><span class="sxs-lookup"><span data-stu-id="92177-114">For example, for version *x.y*, the minor version number is *y*.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="92177-115">コメント</span><span class="sxs-lookup"><span data-stu-id="92177-115">Remarks</span></span>  
 <span data-ttu-id="92177-116">`GetTypeLibInfo`関数は、 [Tlbexp.exe (タイプ ライブラリ エクスポーター)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md)です。</span><span class="sxs-lookup"><span data-stu-id="92177-116">The `GetTypeLibInfo` function is called by the [Tlbexp.exe (Type Library Exporter)](../../../../docs/framework/tools/tlbexp-exe-type-library-exporter.md).</span></span> <span data-ttu-id="92177-117">このツールは、共通言語ランタイム (CLR) アセンブリ内の型を記述するタイプ ライブラリを生成します。</span><span class="sxs-lookup"><span data-stu-id="92177-117">This tool generates a type library that describes the types in a common language runtime (CLR) assembly.</span></span>  
  
 <span data-ttu-id="92177-118">任意のパラメーターが null を返します、`HRESULT`の`E_POINTER`します。</span><span class="sxs-lookup"><span data-stu-id="92177-118">If any parameter is null, the function returns an `HRESULT` of `E_POINTER`.</span></span> <span data-ttu-id="92177-119">返しますそれ以外の場合、`S_OK`です。</span><span class="sxs-lookup"><span data-stu-id="92177-119">Otherwise, it returns `S_OK`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="92177-120">要件</span><span class="sxs-lookup"><span data-stu-id="92177-120">Requirements</span></span>  
 <span data-ttu-id="92177-121">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="92177-121">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="92177-122">**ヘッダー:** TlbRef.h</span><span class="sxs-lookup"><span data-stu-id="92177-122">**Header:** TlbRef.h</span></span>  
  
 <span data-ttu-id="92177-123">**ライブラリ:** TlbRef.lib</span><span class="sxs-lookup"><span data-stu-id="92177-123">**Library:** TlbRef.lib</span></span>  
  
 <span data-ttu-id="92177-124">**.NET framework のバージョン:**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="92177-124">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="92177-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="92177-125">See Also</span></span>  
 [<span data-ttu-id="92177-126">Tlbexp ヘルパー関数します。</span><span class="sxs-lookup"><span data-stu-id="92177-126">Tlbexp Helper Functions</span></span>](../../../../docs/framework/unmanaged-api/tlbexp/index.md)  
 <span data-ttu-id="92177-127">[LoadTypeLibEx 関数](https://msdn.microsoft.com/library/ms221249\(v=vs.85\).aspx)</span><span class="sxs-lookup"><span data-stu-id="92177-127">[LoadTypeLibEx Function](https://msdn.microsoft.com/library/ms221249\(v=vs.85\).aspx)</span></span>