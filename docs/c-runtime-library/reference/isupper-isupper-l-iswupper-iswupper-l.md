---
title: "isupper、_isupper_l、iswupper、_iswupper_l | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- isupper
- iswupper
- _iswupper_l
- _isupper_l
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
- api-ms-win-crt-string-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- isupper
- _istupper
- iswupper
dev_langs:
- C++
helpviewer_keywords:
- istupper function
- iswupper function
- isupper_l function
- _isupper_l function
- iswupper_l function
- _istupper function
- _iswupper_l function
- isupper function
ms.assetid: da2bcc9f-241c-48c0-9a0e-ad273827e16a
caps.latest.revision: 21
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
ms.openlocfilehash: ded3f62cc54e769e9b7ba17bd106a64daf14e63f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/01/2017

---
# <a name="isupper-isupperl-iswupper-iswupperl"></a>isupper、_isupper_l、iswupper、_iswupper_l
整数が大文字を表すかどうかを決定します。  
  
## <a name="syntax"></a>構文  
  
```  
int isupper(  
   int c   
);  
int _isupper_l (  
   int c,  
   _locale_t locale  
);  
int iswupper(  
   wint_t c   
);  
int _iwsupper_l(  
   wint_t c,  
   _locale_t locale   
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `c`  
 テストする整数。  
  
 `locale`  
 使用するロケール。  
  
## <a name="return-value"></a>戻り値  
 これらのルーチンでは、`c` が大文字の特殊表現の場合は 0 以外の値を返します。 `isupper`場合は 0 以外の値を返します`c`は、大文字 (A ~ Z)。 `iswupper` は、`c` が大文字に対応するワイド文字の場合、または `c` が実装定義のワイド文字セットの 1 文字で、かつ c に対して `iswcntrl`、`iswdigit`、`iswpunct`、`iswspace` のすべてが 0 である場合に、0 以外の値を返します。 これらの各ルーチンは、`c` がテスト条件を満たしていない場合は 0 を返します。  
  
 これらの関数のうち `_l` サフィックスが付いているバージョンは、ロケールに依存する動作に現在のロケールではなく渡されたロケールを使用します。 詳細については、「[ロケール](../../c-runtime-library/locale.md)」をご覧ください。  
  
 `isupper` と `_isupper_l` の動作は、`c` が EOF ではなく、かつ、0 ～ 0xFF の範囲でない場合は未定義です。 CRT デバッグ ライブラリを使用し、`c` がこれらの値のうちのいずれかの値でない場合は、アサーションが発生します。  
  
### <a name="generic-text-routine-mappings"></a>汎用テキスト ルーチンのマップ  
  
|TCHAR.H のルーチン|_UNICODE および _MBCS が未定義の場合|_MBCS が定義されている場合|_UNICODE が定義されている場合|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_istupper`|`isupper`|[_ismbcupper](../../c-runtime-library/reference/ismbclower-ismbclower-l-ismbcupper-ismbcupper-l.md)|`iswupper`|  
|`_istupper_l`|`_isupper_l`|[_ismbclower、_ismbclower_l、_ismbcupper、_ismbcupper_l](../../c-runtime-library/reference/ismbclower-ismbclower-l-ismbcupper-ismbcupper-l.md)|`_iswupper_l`|  
  
## <a name="requirements"></a>要件  
  
|ルーチン|必須ヘッダー|  
|-------------|---------------------|  
|`isupper`|\<ctype.h>|  
|`_isupper_l`|\<ctype.h>|  
|`iswupper`|\<ctype.h> または \<wchar.h>|  
|`_iswupper_l`|\<ctype.h>|  
  
 互換性の詳細については、「 [互換性](../../c-runtime-library/compatibility.md)」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [文字分類](../../c-runtime-library/character-classification.md)   
 [ロケール](../../c-runtime-library/locale.md)   
 [is、isw 系ルーチン](../../c-runtime-library/is-isw-routines.md)
