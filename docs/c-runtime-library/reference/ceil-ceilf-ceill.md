---
title: "ceil、ceilf、ceill | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- ceilf
- ceil
- ceill
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
- ceil
- ceilf
- ceill
dev_langs:
- C++
helpviewer_keywords:
- calculating value ceilings
- ceill function
- ceil function
- ceilf function
ms.assetid: f4e5acab-5c8f-4b10-9ae2-9561e6453718
caps.latest.revision: 13
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
ms.openlocfilehash: 1fd4b888c8fc332c07aed62af03b340864dfe3bf
ms.contentlocale: ja-jp
ms.lasthandoff: 03/29/2017

---
# <a name="ceil-ceilf-ceill"></a>ceil、ceilf、ceill
値の切り上げを計算します。  
  
## <a name="syntax"></a>構文  
  
```  
double ceil(   
   double x   
);  
float ceil(  
   float x  
);  // C++ only  
long double ceil(  
   long double x  
);  // C++ only  
float ceilf(  
   float x  
);  
long double ceill(  
   long double x  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `x`  
 浮動小数点値。  
  
## <a name="return-value"></a>戻り値  
 `ceil` 関数は `x` 以上の最も小さい整数を表す浮動小数点値を返します。 エラーの戻り値はありません。  
  
|入力|SEH 例外|Matherr 例外|  
|-----------|-------------------|-----------------------|  
|± `QNAN`,`IND`|none|`_DOMAIN`|  
  
 `ceil` には、ストリーミング SIMD 拡張機能 (SSE2) を使用して実装されています。 SSE2 実装の使い方の詳細および制約については、「[_set_SSE2_enable](../../c-runtime-library/reference/set-sse2-enable.md)」を参照してください。  
  
## <a name="remarks"></a>コメント  
 C++ ではオーバーロードが可能であるため、`ceil` のオーバーロードを呼び出すことができます。 C プログラムでは、`ceil` は常に double を受け取って返します。  
  
## <a name="requirements"></a>要件  
  
|ルーチン|必須ヘッダー|  
|-------------|---------------------|  
|`ceil`、`ceilf`、`ceill`|\<math.h>|  
  
 互換性の詳細については、「[互換性](../../c-runtime-library/compatibility.md)」をご覧ください。  
  
## <a name="example"></a>例  
 「[floor](../../c-runtime-library/reference/floor-floorf-floorl.md)」の例を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [浮動小数点サポート](../../c-runtime-library/floating-point-support.md)   
 [floor、floorf、floorl](../../c-runtime-library/reference/floor-floorf-floorl.md)   
 [fmod、fmodf](../../c-runtime-library/reference/fmod-fmodf.md)   
 [round、roundf、roundl](../../c-runtime-library/reference/round-roundf-roundl.md)
