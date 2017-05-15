---
title: '&lt;istream&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- istream/std::<istream>
- std.<istream>
- <istream>
- std::<istream>
dev_langs:
- C++
helpviewer_keywords:
- istream header
ms.assetid: efcf24e4-05d1-4719-ab0b-9e7ebe845d89
caps.latest.revision: 20
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
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
ms.openlocfilehash: a329d340709ca5d74f6a52c6ee6c8070ef2faa7f
ms.contentlocale: ja-jp
ms.lasthandoff: 04/29/2017

---
# <a name="ltistreamgt"></a>&lt;istream&gt;
iostream の抽出を仲介するテンプレート クラス basic_istream と、挿入と抽出の両方を仲介するテンプレート クラス basic_iostream を定義します。 ヘッダーは、関連するマニピュレーターも定義します。 このヘッダー ファイルは通常、別の iostream ヘッダーに含まれているため、ほとんどの場合、直接含める必要はありません。  
  
## <a name="syntax"></a>構文  
  
```  
#include <istream>  
  
```  
  
### <a name="typedefs"></a>Typedefs  
  
|||  
|-|-|  
|[iostream](../standard-library/istream-typedefs.md#iostream)|`char` に特殊化された型 `basic_iostream`。|  
|[istream](../standard-library/istream-typedefs.md#istream)|`char` に特殊化された型 `basic_istream`。|  
|[wiostream](../standard-library/istream-typedefs.md#wiostream)|**wchar** に特殊化された型 `basic_iostream`。|  
|[wistream](../standard-library/istream-typedefs.md#wistream)|**wchar** に特殊化された型 `basic_istream`。|  
  
### <a name="manipulators"></a>マニピュレーター  
  
|||  
|-|-|  
|[ws](../standard-library/istream-functions.md#ws)|ストリーム内の空白をスキップします。|  
|[swap](../standard-library/istream-functions.md#istream_swap)|2 つのストリーム オブジェクトを交換します。|  
  
### <a name="operators"></a>演算子  
  
|||  
|-|-|  
|[operator>>](../standard-library/istream-operators.md#op_gt_gt)|ストリームから文字と文字列を抽出します。|  
  
### <a name="classes"></a>クラス  
  
|||  
|-|-|  
|[basic_iostream](../standard-library/basic-iostream-class.md)|入力と出力の両方を行うことができるストリーム クラス。|  
|[basic_istream](../standard-library/basic-istream-class.md)|このテンプレート クラスは、**Elem** 型の要素を含むストリーム バッファーからの要素とエンコードされたオブジェクトの抽出を制御するオブジェクトを表します。Elem 型は [char_type](../standard-library/basic-ios-class.md#char_type) とも呼ばれ、その特性は、[traits_type](../standard-library/basic-ios-class.md#traits_type) とも呼ばれるクラス **Tr** によって決定されます。|  
  
## <a name="see-also"></a>関連項目  
 [C++ 標準ライブラリ内のスレッド セーフ](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [iostream プログラミング](../standard-library/iostream-programming.md)   
 [iostreams の規則](../standard-library/iostreams-conventions.md)



