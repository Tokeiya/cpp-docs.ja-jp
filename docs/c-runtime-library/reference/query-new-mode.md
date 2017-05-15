---
title: _query_new_mode | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _query_new_mode
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-heap-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- query_new_mode
- _query_new_mode
dev_langs:
- C++
helpviewer_keywords:
- query_new_mode function
- handler modes
- _query_new_mode function
ms.assetid: e185c5f9-b73b-4257-8eff-b47648374768
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: 414bbd73f44a51ab1ec35c9fb2bd8b3914c1ea8d
ms.contentlocale: ja-jp
ms.lasthandoff: 03/29/2017

---
# <a name="querynewmode"></a>_query_new_mode
`malloc` に対して `_set_new_mode` によって設定された新しいハンドラー モードを示す整数を返します。  
  
## <a name="syntax"></a>構文  
  
```  
  
      int _query_new_mode(  
   void   
);  
```  
  
## <a name="return-value"></a>戻り値  
 `malloc` に対して現在の新しいハンドラー モード、つまり 0 または 1 を返します。 戻り値 1 は、メモリの割り当てに失敗したときに、`malloc` が新しいハンドラー ルーチンを呼び出すことを指定し、戻り値 0 は呼び出さないことを指定します。  
  
## <a name="remarks"></a>コメント  
 C++ の `_query_new_mode` 関数は、[malloc](../../c-runtime-library/reference/malloc.md) に対して C++ の [_set_new_mode](../../c-runtime-library/reference/set-new-mode.md) 関数によって設定された新しいハンドラー モードを示す整数を返します。 新しいハンドラー モードは、メモリの割り当てに失敗したときに、`malloc` が [_set_new_handler](../../c-runtime-library/reference/set-new-handler.md) によって設定された新しいハンドラー ルーチンを呼び出すかどうかを指定します。 既定では、`malloc` は、エラーの際に新しいハンドラー ルーチンを呼び出しません。 `_set_new_mode` を使用してこの動作をオーバーライドすると、**new** 演算子がメモリの割り当てに失敗したときと同じ方法で、エラー発生時に `malloc` によって新しいハンドラー ルーチンを呼び出すことができます。 詳細については、C++ 言語リファレンスの「[new および delete 演算子](../../cpp/new-and-delete-operators.md)」の説明をご覧ください。  
  
## <a name="requirements"></a>要件  
  
|ルーチン|必須ヘッダー|  
|-------------|---------------------|  
|`_query_new_mode`|\<new.h>|  
  
 互換性の詳細については、概要の「[互換性](../../c-runtime-library/compatibility.md)」をご覧ください。  
  
## <a name="libraries"></a>ライブラリ  
 [C ランタイム ライブラリ](../../c-runtime-library/crt-library-features.md)のすべてのバージョン。  
  
## <a name="see-also"></a>関連項目  
 [メモリ割り当て](../../c-runtime-library/memory-allocation.md)   
 [calloc](../../c-runtime-library/reference/calloc.md)   
 [free](../../c-runtime-library/reference/free.md)   
 [realloc](../../c-runtime-library/reference/realloc.md)   
 [_query_new_handler](../../c-runtime-library/reference/query-new-handler.md)