---
title: "erf、erff、erfl、erfc、erfcf、erfcl | Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- erff
- erfl
- erf
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
- erfl
- erf
- erff
dev_langs:
- C++
helpviewer_keywords:
- erfl function
- erff function
- erf function
ms.assetid: 144d90d3-e437-41c2-a659-cd57596023b5
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 16d1bf59dfd4b3ef5f037aed9c0f6febfdf1a2e8
ms.openlocfilehash: de987b726a4a25fa3bc23bbb569e7c9a9138de2b
ms.contentlocale: ja-jp
ms.lasthandoff: 10/09/2017

---
# <a name="erf-erff-erfl-erfc-erfcf-erfcl"></a>erf、erff、erfl、erfc、erfcf、erfcl
値の誤差関数または相補誤差関数を計算します。  
  
## <a name="syntax"></a>構文  
  
```  
double erf(  
   double x  
);  
float erf(  
   float x  
); // C++ only  
long double erf(  
   long double x  
); // C++ only  
float erff(  
   float x  
);  
long double erfl(  
   long double x  
);  
double erfc(  
   double x  
);  
float erfc(  
   float x  
); // C++ only  
long double erfc(  
   long double x  
); // C++ only  
float erfcf(  
   float x  
);  
long double erfcl(  
   long double x  
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `x`  
 浮動小数点値。  
  
## <a name="return-value"></a>戻り値  
 `erf` 関数は、`x` のガウスの誤差関数を返します。 `erfc` 関数は、`x` のガウスの相補誤差関数を返します。  
  
## <a name="remarks"></a>コメント  
 `erf` 関数は、次のように定義されているガウスの誤差関数を計算します。  
  
 ![x の誤差関数](../../c-runtime-library/reference/media/crt_erf_formula.PNG "CRT_erf_formula")  
  
 ガウスの相補誤差関数が 1 - として定義されている erf (x)。 `erf` 関数は、-1.0 ～ 1.0 の範囲の値を返します。 エラーの戻り値はありません。 `erfc` 関数は、0 ～ 2 の範囲の値を返します。 `x` が `erfc` に対して大きすぎる場合、`errno` 変数は `ERANGE` に設定されます。  
  
 C++ ではオーバーロードが可能であるため、`erf` 型と `erfc` 型を受け取って返す `float` と `long double` のオーバーロードを呼び出すことができます。 C プログラムでは、`erf` および `erfc` は常に `double` を受け取って返します。  
  
## <a name="requirements"></a>要件  
  
|関数|必須ヘッダー|  
|--------------|---------------------|  
|`erf`, `erff`, `erfl`, `erfc`, `erfcf`, `erfcl`|\<math.h>|  
  
 互換性の詳細については、「 [互換性](../../c-runtime-library/compatibility.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [浮動小数点サポート](../../c-runtime-library/floating-point-support.md)
