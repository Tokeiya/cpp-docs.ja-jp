---
title: _set_SSE2_enable | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _set_SSE2_enable
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
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _set_SSE2_enable
- set_SSE2_enable
dev_langs:
- C++
helpviewer_keywords:
- _set_SSE2_enable function
- Streaming SIMD Extensions 2 instructions
- set_SSE2_enable function
ms.assetid: 55db895d-fc1e-475a-9110-b781a9bb51c5
caps.latest.revision: 19
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: e257f037a05c45f5b98e64ea55bd125af443b0be
ms.openlocfilehash: 6dcc32b981c73cda13152f82139a307e4739fe5c
ms.contentlocale: ja-jp
ms.lasthandoff: 03/29/2017

---
# <a name="setsse2enable"></a>_set_SSE2_enable
CRT 数値演算ルーチンで [ストリーミング SIMD 拡張命令 2](http://msdn.microsoft.com/en-us/f98440eb-73a9-4f96-b203-ac41bb6701ea) (SSE2) 命令の使用を有効または無効にします。 (この関数は、x64 アーキテクチャでは利用できません。SSE2 が既定で有効になっているためです。)  
  
## <a name="syntax"></a>構文  
  
```  
int _set_SSE2_enable(  
   int flag  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `flag`  
 SSE2 実装を有効にする場合は 1、SSE2 実装を無効にする場合は 0。 既定では、SSE2 実装はこれをサポートするプロセッサでは有効です。  
  
## <a name="return-value"></a>戻り値  
 SSE2 実装が有効な場合はゼロ以外、SSE2 実装が無効になっている場合はゼロを返します。  
  
## <a name="remarks"></a>コメント  
 次の関数には、`_set_SSE2_enable` を使用して有効にできる SSE2 実装があります。  
  
-   [atan](../../c-runtime-library/reference/atan-atanf-atanl-atan2-atan2f-atan2l.md)  
  
-   [ceil](../../c-runtime-library/reference/ceil-ceilf-ceill.md)  
  
-   [exp](../../c-runtime-library/reference/exp-expf.md)  
  
-   [floor](../../c-runtime-library/reference/floor-floorf-floorl.md)  
  
-   [log](../../c-runtime-library/reference/log-logf-log10-log10f.md)  
  
-   [log10](../../c-runtime-library/reference/log-logf-log10-log10f.md)  
  
-   [modf](../../c-runtime-library/reference/modf-modff-modfl.md)  
  
-   [pow](../../c-runtime-library/reference/pow-powf-powl.md)  
  
 これらの関数の SSE2 実装では、既定の実装とは若干異なる回答が生じる場合があります。SSE2 の中間値は 64 ビットの浮動小数点数ですが、既定の実装の中間値は、80 ビットの浮動小数点数であるためです。  
  
> [!NOTE]
>  [/Oi (組み込み関数の生成)](../../build/reference/oi-generate-intrinsic-functions.md) コンパイラ オプションを使用してプロジェクトをコンパイルする場合、`_set_SSE2_enable` では何も生じないように見えることがあります。 `/Oi` コンパイラ オプションは、CRT 呼び出しを置き換えるための組み込み関数を使用する権限をコンパイラに与えます。この動作は `_set_SSE2_enable` の効果を上書きするものです。 `/Oi` が `_set_SSE2_enable` を上書きしないようにするには、`/Oi-` を使用してプロジェクトをコンパイルします。 `/Oi` を暗黙指定する他のコンパイラ スイッチを使用するときにも、そのようにすることをお勧めします。  
  
 SSE2 実装はすべての例外がマスクされる場合にのみ使用します。 例外をマスクするには、[_control87、_controlfp](../../c-runtime-library/reference/control87-controlfp-control87-2.md) を使用します。  
  
## <a name="requirements"></a>要件  
  
|ルーチン|必須ヘッダー|  
|-------------|---------------------|  
|`_set_SSE2_enable`|\<math.h>|  
  
 互換性について詳しくは、「はじめに」の「[互換性](../../c-runtime-library/compatibility.md)」をご覧ください。  
  
## <a name="example"></a>例  
  
```  
// crt_set_SSE2_enable.c  
// processor: x86  
#include <math.h>  
#include <stdio.h>  
  
int main()  
{  
   int i = _set_SSE2_enable(1);  
  
   if (i)  
      printf("SSE2 enabled.\n");  
   else  
      printf("SSE2 not enabled; processor does not support SSE2.\n");  
}  
```  
  
 **出力**  
  
 `SSE2 enabled.`  
  
## <a name="see-also"></a>関連項目  
 [CRT ライブラリの機能](../../c-runtime-library/crt-library-features.md)