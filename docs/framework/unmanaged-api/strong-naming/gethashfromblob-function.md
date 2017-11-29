---
title: "GetHashFromBlob 関数"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: GetHashFromBlob
api_location: mscoree.dll
api_type: DLLExport
f1_keywords: GetHashFromBlob
helpviewer_keywords: GetHashFromBlob function [.NET Framework strong naming]
ms.assetid: b712d862-f2d0-4b55-87d4-65bbeadef982
topic_type: apiref
caps.latest.revision: "14"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 360036cd1578c2845f09f92c09d79e44618abe75
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/21/2017
---
# <a name="gethashfromblob-function"></a><span data-ttu-id="e1782-102">GetHashFromBlob 関数</span><span class="sxs-lookup"><span data-stu-id="e1782-102">GetHashFromBlob Function</span></span>
<span data-ttu-id="e1782-103">指定したハッシュ アルゴリズムを使用して、指定されたメモリ アドレスのアセンブリのハッシュを取得します。</span><span class="sxs-lookup"><span data-stu-id="e1782-103">Gets a hash of the assembly at the specified memory address, using the specified hash algorithm.</span></span>  
  
 <span data-ttu-id="e1782-104">この関数は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="e1782-104">This function has been deprecated.</span></span> <span data-ttu-id="e1782-105">使用して、 [ICLRStronName::GetHashFromBlob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromblob-method.md)メソッド代わりにします。</span><span class="sxs-lookup"><span data-stu-id="e1782-105">Use the [ICLRStronName::GetHashFromBlob](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromblob-method.md) method instead.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e1782-106">構文</span><span class="sxs-lookup"><span data-stu-id="e1782-106">Syntax</span></span>  
  
```  
HRESULT GetHashFromBlob (  
    [in]  BYTE    *pbBlob,  
    [in]  DWORD   cchBlob,  
    [in, out] unsigned int   *piHashAlg,  
    [out] BYTE    *pbHash,  
    [in]  DWORD   cchHash,  
    [out] DWORD   *pchHash  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e1782-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e1782-107">Parameters</span></span>  
 `pbBlob`  
 <span data-ttu-id="e1782-108">[in]ハッシュされるメモリ ブロックのアドレスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e1782-108">[in] A pointer to the address of the memory block to be hashed.</span></span>  
  
 `cchBlob`  
 <span data-ttu-id="e1782-109">[in]メモリ ブロックの長さ、(バイト単位)。</span><span class="sxs-lookup"><span data-stu-id="e1782-109">[in] The length, in bytes, of the memory block.</span></span>  
  
 `piHashAlg`  
 <span data-ttu-id="e1782-110">[入力、出力].ハッシュ アルゴリズムを指定する定数。</span><span class="sxs-lookup"><span data-stu-id="e1782-110">[in, out] A constant that specifies the hash algorithm.</span></span> <span data-ttu-id="e1782-111">既定のアルゴリズムに 0 を使用します。</span><span class="sxs-lookup"><span data-stu-id="e1782-111">Use zero for the default algorithm.</span></span>  
  
 `pbHash`  
 <span data-ttu-id="e1782-112">[out]返されるハッシュ バッファー。</span><span class="sxs-lookup"><span data-stu-id="e1782-112">[out] The returned hash buffer.</span></span>  
  
 `cchHash`  
 <span data-ttu-id="e1782-113">[in]場合は、要求された最大サイズ`pbHash`です。</span><span class="sxs-lookup"><span data-stu-id="e1782-113">[in] The requested maximum size of `pbHash`.</span></span>  
  
 `pchHash`  
 <span data-ttu-id="e1782-114">[out]サイズ (バイト単位)、返された`pbHash`です。</span><span class="sxs-lookup"><span data-stu-id="e1782-114">[out] The size, in bytes, of the returned `pbHash`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e1782-115">要件</span><span class="sxs-lookup"><span data-stu-id="e1782-115">Requirements</span></span>  
 <span data-ttu-id="e1782-116">**プラットフォーム:**を参照してください[システム要件](../../../../docs/framework/get-started/system-requirements.md)です。</span><span class="sxs-lookup"><span data-stu-id="e1782-116">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e1782-117">**ヘッダー:** StrongName.h</span><span class="sxs-lookup"><span data-stu-id="e1782-117">**Header:** StrongName.h</span></span>  
  
 <span data-ttu-id="e1782-118">**ライブラリ:** MsCorEE.dll にリソースとして含まれています。</span><span class="sxs-lookup"><span data-stu-id="e1782-118">**Library:** Included as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e1782-119">**.NET framework のバージョン:**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e1782-119">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e1782-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="e1782-120">See Also</span></span>  
 [<span data-ttu-id="e1782-121">GetHashFromBlob メソッド</span><span class="sxs-lookup"><span data-stu-id="e1782-121">GetHashFromBlob Method</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-gethashfromblob-method.md)  
 [<span data-ttu-id="e1782-122">ICLRStrongName インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e1782-122">ICLRStrongName Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)