---
title: "浮動小数点サポート | Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: c.math
dev_langs: C++
helpviewer_keywords:
- floating-point numbers, math routines
- math routines
- floating-point numbers
ms.assetid: e4fcaf69-5c8e-4854-a9bb-1f412042131e
caps.latest.revision: "17"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 60a2131b08b9f0ac119bdcd414f2d4d1761a9b6c
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="floating-point-support"></a>浮動小数点サポート
Microsoft C ランタイム ライブラリ (CRT) では、ISO C99 で必要とされる関数をすべて含む、多数の浮動小数点数値演算ライブラリ関数を提供しています。 これらの関数は、正確性とパフォーマンスのバランスをとるために実装されます。 正確に丸めた結果を生成するには非常にコストがかかる場合があるため、正確に丸めた結果の近似値を効率的に生成できるように当該関数が設計されました。 ほとんどのケースでは、生成される結果は正確に丸めた結果の +/- 1 ulp の誤差範囲内に収まります。ただし、不正確さがそれより大きくなる場合もあります。  
  
 浮動小数点数値演算ライブラリ関数の多くは、CPU アーキテクチャの種類に応じて実装の種類も異なります。 たとえば、32 ビット x86 CRT の実装は、64 ビット x64 CRT の実装とは異なります。 さらに、関数の中には特定の CPU アーキテクチャに対して複数の実装が用意されているものもあります。 CPU でサポートされている命令セットに応じて実行時に動的に実装を選択するのが最も効率的な方法です。 たとえば、32 ビット x86 CRT で、一部の関数には x87 実装と SSE2 実装の両方が用意されています。 SSE2 をサポートしている CPU で実行すると、速い方の SSE2 実装が使用されます。 SSE2 をサポートしていない CPU で実行すると、遅い方の x87 実装が使用されます。 数値演算ライブラリ関数の実装の種類が異なると、結果を生成するために使用する CPU 命令およびアルゴリズムも異なる場合があります。このため、CPU 間で、関数の生成する結果が異なる場合があります。 ほとんどの場合、結果は正確に丸めた結果の +/- 1 ulp の誤差範囲内に収まります。ただし、実際の結果は、CPU 間で異なる場合があります。  
  
 以前の 16 ビット バージョンの Microsoft C/C++ および Microsoft Visual C++ では、80 ビット精度浮動小数点データ型として `long double` 型をサポートしていました。 最近のバージョンの Visual C++ では、`long double` データ型は、`double` 型と同じ 64 ビット精度浮動小数点データ型となっています。 コンパイラは、`long double` と `double` を異なる型として扱いますが、`long double` 関数は、対応する `double` 関数と同じものとなります。 CRT では、ISO C99 ソース コードの互換性を維持するために `long double` バージョンの数値演算関数を提供しています。ただし、そのバイナリ表現は他のコンパイラと異なる場合があるので注意してください。  
  
 CRT では、以下の浮動小数点関数をサポートしています。  
  
 [abs、labs、llabs、_abs64](../c-runtime-library/reference/abs-labs-llabs-abs64.md)  
  
 [acos、acosf、acosl](../c-runtime-library/reference/acos-acosf-acosl.md)  
  
 [acosh、acoshf、acoshl](../c-runtime-library/reference/acosh-acoshf-acoshl.md)  
  
 [asin、asinf、asinl](../c-runtime-library/reference/asin-asinf-asinl.md)  
  
 [asinh、asinhf、asinhl](../c-runtime-library/reference/asinh-asinhf-asinhl.md)  
  
 [atan、atanf、atanl、atan2、atan2f、atan2l](../c-runtime-library/reference/atan-atanf-atanl-atan2-atan2f-atan2l.md)  
  
 [atanh、atanhf、atanhl](../c-runtime-library/reference/atanh-atanhf-atanhl.md)  
  
 [_atodbl、_atodbl_l](../c-runtime-library/reference/atodbl-atodbl-l-atoldbl-atoldbl-l-atoflt-atoflt-l.md)  
  
 [atof、_atof_l](../c-runtime-library/reference/atof-atof-l-wtof-wtof-l.md)  
  
 [_atoflt、_atoflt_l、_atoldbl、_atoldbl_l](../c-runtime-library/reference/atodbl-atodbl-l-atoldbl-atoldbl-l-atoflt-atoflt-l.md)  
  
 [cbrt、cbrtf、cbrtl](../c-runtime-library/reference/cbrt-cbrtf-cbrtl.md)  
  
 [ceil、ceilf、ceill](../c-runtime-library/reference/ceil-ceilf-ceill.md)  
  
 [_chgsign、_chgsignf、_chgsignl](../c-runtime-library/reference/chgsign-chgsignf-chgsignl.md)  
  
 [_clear87、_clearfp](../c-runtime-library/reference/clear87-clearfp.md)  
  
 [compl](../c-runtime-library/reference/compl.md)  
  
 [conj、conjf、conjl](../c-runtime-library/reference/conj-conjf-conjl.md)  
  
 [_control87、\__control87_2、_controlfp](../c-runtime-library/reference/control87-controlfp-control87-2.md)  
  
 [_controlfp_s](../c-runtime-library/reference/controlfp-s.md)  
  
 [copysign、copysignf、copysignl、_copysign、_copysignf、_copysignl](../c-runtime-library/reference/copysign-copysignf-copysignl-copysign-copysignf-copysignl.md)  
  
 [cos、cosf、cosl](../c-runtime-library/reference/cos-cosf-cosl-cosh-coshf-coshl.md)  
  
 [cosh、coshf、coshl](../c-runtime-library/reference/cos-cosf-cosl-cosh-coshf-coshl.md)  
  
 [div](../c-runtime-library/reference/div.md)  
  
 [_ecvt](../c-runtime-library/reference/ecvt.md)  
  
 [ecvt](../c-runtime-library/reference/posix-ecvt.md)  
  
 [_ecvt_s](../c-runtime-library/reference/ecvt-s.md)  
  
 [erf、erff、erfl、erfc、erfcf、erfcl](../c-runtime-library/reference/erf-erff-erfl-erfc-erfcf-erfcl.md)  
  
 [exp、expf、expl](../c-runtime-library/reference/exp-expf.md)  
  
 [exp2、exp2f、exp2l](../c-runtime-library/reference/exp2-exp2f-exp2l.md)  
  
 [expm1、expm1f、expm1l](../c-runtime-library/reference/expm1-expm1f-expm1l.md)  
  
 [fabs、fabsf](../c-runtime-library/reference/fabs-fabsf-fabsl.md)  
  
 [_fcvt](../c-runtime-library/reference/fcvt.md)  
  
 [fcvt](../c-runtime-library/reference/posix-fcvt.md)  
  
 [_fcvt_s](../c-runtime-library/reference/fcvt-s.md)  
  
 [fdim、fdimf、fdiml](../c-runtime-library/reference/fdim-fdimf-fdiml.md)  
  
 [feclearexcept](../c-runtime-library/reference/feclearexcept1.md)  
  
 [fegetenv](../c-runtime-library/reference/fegetenv1.md)  
  
 [fegetexceptflag](../c-runtime-library/reference/fegetexceptflag2.md)  
  
 [fegetround](../c-runtime-library/reference/fegetround-fesetround2.md)  
  
 [feholdexcept](../c-runtime-library/reference/feholdexcept2.md)  
  
 [feraiseexcept](../c-runtime-library/reference/feraiseexcept.md)  
  
 [ferror](../c-runtime-library/reference/ferror.md)  
  
 [fesetenv](../c-runtime-library/reference/fesetenv1.md)  
  
 [fesetexceptflag](../c-runtime-library/reference/fesetexceptflag2.md)  
  
 [fesetround](../c-runtime-library/reference/fegetround-fesetround2.md)  
  
 [fetestexcept](../c-runtime-library/reference/fetestexcept1.md)  
  
 [feupdateenv](../c-runtime-library/reference/feupdateenv.md)  
  
 [_finite、_finitef](../c-runtime-library/reference/finite-finitef.md)  
  
 [floor、floorf、floorl](../c-runtime-library/reference/floor-floorf-floorl.md)  
  
 [fma、fmaf、fmal](../c-runtime-library/reference/fma-fmaf-fmal.md)  
  
 [fmax、fmaxf、fmaxl](../c-runtime-library/reference/fmax-fmaxf-fmaxl.md)  
  
 [fmin、fminf、fminl](../c-runtime-library/reference/fmin-fminf-fminl.md)  
  
 [fmod、fmodf](../c-runtime-library/reference/fmod-fmodf.md)  
  
 [_fpclass、_fpclassf](../c-runtime-library/reference/fpclass-fpclassf.md)  
  
 [fpclassify](../c-runtime-library/reference/fpclassify.md)  
  
 [_fpieee_flt](../c-runtime-library/reference/fpieee-flt.md)  
  
 [_fpreset](../c-runtime-library/reference/fpreset.md)  
  
 [frexp](../c-runtime-library/reference/frexp.md)  
  
 [gcvt](../c-runtime-library/reference/posix-gcvt.md)  
  
 [_gcvt](../c-runtime-library/reference/gcvt.md)  
  
 [_gcvt_s](../c-runtime-library/reference/gcvt-s.md)  
  
 [_get_FMA3_enable、_set_FMA3_enable](../c-runtime-library/reference/get-fma3-enable-set-fma3-enable.md)  
  
 [hypot、hypotf、hypotl、_hypot、_hypotf、_hypotl](../c-runtime-library/reference/hypot-hypotf-hypotl-hypot-hypotf-hypotl.md)  
  
 [ilogb、ilogbf、ilogbl](../c-runtime-library/reference/ilogb-ilogbf-ilogbl2.md)  
  
 [imaxabs](../c-runtime-library/reference/imaxabs.md)  
  
 [imaxdiv](../c-runtime-library/reference/imaxdiv.md)  
  
 [isnan、_isnan、_isnanf](../c-runtime-library/reference/isnan-isnan-isnanf.md)  
  
 [_j0、_j1、_jn](../c-runtime-library/reference/bessel-functions-j0-j1-jn-y0-y1-yn.md)  
  
 [ldexp](../c-runtime-library/reference/ldexp.md)  
  
 [ldiv、lldiv](../c-runtime-library/reference/ldiv-lldiv.md)  
  
 [lgamma、lgammaf、lgammal](../c-runtime-library/reference/lgamma-lgammaf-lgammal.md)  
  
 [llrint、llrintf、llrintl](../c-runtime-library/reference/lrint-lrintf-lrintl-llrint-llrintf-llrintl.md)  
  
 [llround、llroundf、llroundl](../c-runtime-library/reference/lround-lroundf-lroundl-llround-llroundf-llroundl.md)  
  
 [log、logf、log10、log10f](../c-runtime-library/reference/log-logf-log10-log10f.md)  
  
 [log1p、log1pf、log1pl](../c-runtime-library/reference/log1p-log1pf-log1pl2.md)  
  
 [log2、log2f、log2l](../c-runtime-library/reference/log2-log2f-log2l.md)  
  
 [logb、logbf、logbl、_logb、_logbf](../c-runtime-library/reference/logb-logbf-logbl-logb-logbf.md)  
  
 [lrint、lrintf、lrintl](../c-runtime-library/reference/lrint-lrintf-lrintl-llrint-llrintf-llrintl.md)  
  
 [_lrotl、_lrotr](../c-runtime-library/reference/lrotl-lrotr.md)  
  
 [lround、lroundf、lroundl](../c-runtime-library/reference/lround-lroundf-lroundl-llround-llroundf-llroundl.md)  
  
 [_matherr](../c-runtime-library/reference/matherr.md)  
  
 [__max](../c-runtime-library/reference/max.md)  
  
 [__min](../c-runtime-library/reference/min.md)  
  
 [modf、modff](../c-runtime-library/reference/modf-modff-modfl.md)  
  
 [nan、nanf、nanl](../c-runtime-library/reference/nan-nanf-nanl.md)  
  
 [nanf](../c-runtime-library/reference/nan-nanf-nanl.md)  
  
 [nanl](../c-runtime-library/reference/nan-nanf-nanl.md)  
  
 [nearbyint、nearbyintf、nearbyintl](../c-runtime-library/reference/nearbyint-nearbyintf-nearbyintl1.md)  
  
 [nextafter、nextafterf、nextafterl、_nextafter、_nextafterf、nexttoward、nexttowardf、nexttowardl](../c-runtime-library/reference/nextafter-functions.md)  
  
 [norm、normf、norml](../c-runtime-library/reference/norm-normf-norml1.md)  
  
 [pow、powf、powl](../c-runtime-library/reference/pow-powf-powl.md)  
  
 [remainder、remainderf、remainderl](../c-runtime-library/reference/remainder-remainderf-remainderl.md)  
  
 [remquo、remquof、remquol](../c-runtime-library/reference/remquo-remquof-remquol.md)  
  
 [rint、rintf、rintl](../c-runtime-library/reference/rint-rintf-rintl.md)  
  
 [_rotl、_rotl64、_rotr、_rotr64](../c-runtime-library/reference/rotl-rotl64-rotr-rotr64.md)  
  
 [round、roundf、roundl](../c-runtime-library/reference/round-roundf-roundl.md)  
  
 [_scalb](../c-runtime-library/reference/scalb.md)  
  
 [scalbn、scalbnf、scalbnl、scalbln、scalblnf、scalblnl](../c-runtime-library/reference/scalbn-scalbnf-scalbnl-scalbln-scalblnf-scalblnl.md)  
  
 [_set_controlfp](../c-runtime-library/reference/set-controlfp.md)  
  
 [_set_SSE2_enable](../c-runtime-library/reference/set-sse2-enable.md)  
  
 [sin、sinf、sinl](../c-runtime-library/reference/sin-sinf-sinl-sinh-sinhf-sinhl.md)  
  
 [sinh、sinhf、sinhl](../c-runtime-library/reference/sin-sinf-sinl-sinh-sinhf-sinhl.md)  
  
 [sqrt、sqrtf、sqrtl](../c-runtime-library/reference/sqrt-sqrtf-sqrtl.md)  
  
 [_status87、_statusfp、_statusfp2](../c-runtime-library/reference/status87-statusfp-statusfp2.md)  
  
 [strtof、_strtof_l](../c-runtime-library/reference/strtof-strtof-l-wcstof-wcstof-l.md)  
  
 [strtold、_strtold_l](../c-runtime-library/reference/strtold-strtold-l-wcstold-wcstold-l.md)  
  
 [tan、tanf、tanl](../c-runtime-library/reference/tan-tanf-tanl-tanh-tanhf-tanhl.md)  
  
 [tanh、tanhf、tanhl](../c-runtime-library/reference/tan-tanf-tanl-tanh-tanhf-tanhl.md)  
  
 [tgamma、tgammaf、tgammal](../c-runtime-library/reference/tgamma-tgammaf-tgammal.md)  
  
 [trunc、truncf、truncl](../c-runtime-library/reference/trunc-truncf-truncl.md)  
  
 [_wtof、_wtof_l](../c-runtime-library/reference/atof-atof-l-wtof-wtof-l.md)  
  
 [_y0、_y1、_yn](../c-runtime-library/reference/bessel-functions-j0-j1-jn-y0-y1-yn.md)  
  
## <a name="see-also"></a>関連項目  
 [カテゴリ別ランタイム ルーチン](../c-runtime-library/run-time-routines-by-category.md)