---
title: ldexp | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- ldexp
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
- ldexp
- _ldexpl
dev_langs:
- C++
helpviewer_keywords:
- calculating real numbers
- computing real numbers
- mantissas, floating-point variables
- ldexp function
- exponent, floating-point numbers
- floating-point functions, mantissa and exponent
ms.assetid: aa7f5310-3879-4f63-ae74-86a39fbdedfa
caps.latest.revision: 12
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
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: 567098b286ba81f2bdd091706518f812f9d2e128
ms.contentlocale: ja-jp
ms.lasthandoff: 04/01/2017

---
# <a name="ldexp"></a>ldexp
浮動小数点数に整数である 2 の累乗を乗算します。  
  
## <a name="syntax"></a>構文  
  
```  
double ldexp(  
   double x,  
   int exp   
);  
float ldexp(  
   float x,  
   int exp  
);  // C++ only  
long double ldexp(  
   long double x,  
   int exp  
);  // C++ only   
float ldexpf(  
   float x,  
   int exp  
);   
long double ldexpl(  
   long double x,  
   int exp  
);   
```  
  
#### <a name="parameters"></a>パラメーター  
 `x`  
 浮動小数点値。  
  
 `exp`  
 整数の指数。  
  
## <a name="return-value"></a>戻り値  
 `ldexp` 関数は、成功した場合、`x` * 2<sup>exp</sup> の値を返します。 オーバーフローについてとの符号に応じて`x`、 `ldexp` +/-返します`HUGE_VAL`;`errno`値に設定されて`ERANGE`です。  
  
 `errno` および考えられるエラー戻り値の詳細については、「[errno、_doserrno、_sys_errlist、_sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)」をご覧ください。  
  
## <a name="remarks"></a>コメント  
 C++ ではオーバーロードが可能であるため、`ldexp` または `float` 型を受け取る `long double` のオーバーロードを呼び出すことができます。 C プログラムでは、`ldexp` は常に `double` および `int` を受け取って `double` を返します。  
  
## <a name="requirements"></a>要件  
  
|ルーチン|C ヘッダー|C++ ヘッダー|  
|-------------|--------------|------------------|  
|`ldexp`、`ldexpf`、`ldexpl`|\<math.h>|\<cmath>|  
  
 互換性の詳細については、「[互換性](../../c-runtime-library/compatibility.md)」をご覧ください。  
  
## <a name="example"></a>例  
  
```  
// crt_ldexp.c  
  
#include <math.h>  
#include <stdio.h>  
  
int main( void )  
{  
   double x = 4.0, y;  
   int p = 3;  
  
   y = ldexp( x, p );  
   printf( "%2.1f times two to the power of %d is %2.1f\n", x, p, y );  
}  
```  
  
## <a name="output"></a>出力  
  
```  
4.0 times two to the power of 3 is 32.0  
```  
  
## <a name="see-also"></a>関連項目  
 [浮動小数点サポート](../../c-runtime-library/floating-point-support.md)   
 [frexp](../../c-runtime-library/reference/frexp.md)   
 [modf、modff、modfl](../../c-runtime-library/reference/modf-modff-modfl.md)