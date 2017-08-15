---
title: "nothrow_t 構造体 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- nothrow_t
dev_langs:
- C++
helpviewer_keywords:
- nothrow_t class
ms.assetid: dc7d5d42-ed5a-4919-88fe-bbad519b7a1d
caps.latest.revision: 20
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
ms.sourcegitcommit: 66798adc96121837b4ac2dd238b9887d3c5b7eef
ms.openlocfilehash: 69b654efb796b567f6a24ca2b6d2b65139a3a8c8
ms.contentlocale: ja-jp
ms.lasthandoff: 04/29/2017

---
# <a name="nothrowt-structure"></a>nothrow_t 構造体
この構造体は operator new の関数パラメーターとして使用し、関数に対して、割り当て失敗を報告する際に例外をスローするのではなく Null ポインター を返すように指定します。  
  
## <a name="syntax"></a>構文  
  
```
struct std::nothrow_t {};
```  
  
## <a name="remarks"></a>コメント  
 この構造体により、コンパイラが適切なバージョンのコンストラクターを選択できます。 [nothrow](../standard-library/new-functions.md#nothrow) は、`std::nothrow_t` 型のオブジェクトと同義です。  
  
## <a name="example"></a>例  
 `std::nothrow_t` を関数パラメーターとして使用する方法の例については、[operator new](../standard-library/new-operators.md#op_new) および [operator new&#91;&#93;](../standard-library/new-operators.md#op_new_arr) に関する記事をご覧ください。  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<new>  
  
 **名前空間:** std  
  
## <a name="see-also"></a>関連項目  
 [C++ 標準ライブラリ内のスレッド セーフ](../standard-library/thread-safety-in-the-cpp-standard-library.md)



