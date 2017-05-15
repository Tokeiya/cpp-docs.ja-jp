---
title: _heapadd | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _heapadd
apilocation:
- msvcr100.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr80.dll
- msvcrt.dll
- msvcr110.dll
- msvcr90.dll
apitype: DLLExport
f1_keywords:
- heapadd
- _heapadd
dev_langs:
- C++
helpviewer_keywords:
- _heapadd function
- memory, adding to heaps
- heaps, adding memory
- heapadd function
ms.assetid: 4d691fe2-2763-49f4-afb1-62738b7cd3ff
caps.latest.revision: 11
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Human Translation
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: 8e5b9c8871d77e4c677c2ad88a8616d0cd9b3eac
ms.lasthandoff: 04/01/2017

---
# <a name="heapadd"></a>_heapadd
ヒープにメモリを追加します。  
  
> [!IMPORTANT]
>  これは古い関数です。 Visual Studio 2015 以降、CRT で使用できません。  
  
## <a name="syntax"></a>構文  
  
```  
int _heapadd(   
   void *memblock,  
   size_t size   
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `memblock`  
 ヒープ メモリへのポインター。  
  
 `size`  
 追加するメモリのサイズ (バイト単位)。  
  
## <a name="return-value"></a>戻り値  
 成功すると、`_heapadd` は 0 を返します。それ以外の場合、この関数は -1 を返し、`errno` を `ENOSYS` に設定します。  
  
 このリターン コードとその他のリターン コードの詳細については、「[_doserrno、errno、_sys_errlist、_sys_nerr](../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)」をご覧ください。  
  
## <a name="remarks"></a>コメント  
 Visual C++ のバージョン 4.0 以降では、新しいデバッグ機能をサポートするために、基になるヒープ構造が C ランタイム ライブラリに移動しました。 その結果、 `_heapadd` は、Win32 API に基づいているすべてのプラットフォームでサポートされなくなりました。  
  
## <a name="requirements"></a>要件  
  
|ルーチン|必須ヘッダー|オプション ヘッダー|  
|-------------|---------------------|---------------------|  
|`_heapadd`|\<malloc.h>|\<errno.h>|  
  
 互換性について詳しくは、「はじめに」の「[互換性](../c-runtime-library/compatibility.md)」をご覧ください。  
  
## <a name="see-also"></a>関連項目  
 [メモリ割り当て](../c-runtime-library/memory-allocation.md)   
 [free](../c-runtime-library/reference/free.md)   
 [_heapchk](../c-runtime-library/reference/heapchk.md)   
 [_heapmin](../c-runtime-library/reference/heapmin.md)   
 [_heapset](../c-runtime-library/heapset.md)   
 [_heapwalk](../c-runtime-library/reference/heapwalk.md)   
 [malloc](../c-runtime-library/reference/malloc.md)   
 [realloc](../c-runtime-library/reference/realloc.md)