---
title: "トークンの評価 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- tokens, evaluating
ms.assetid: 28870b62-dff6-4644-8b75-d58f340b48d2
caps.latest.revision: 8
author: mikeblome
ms.author: mblome
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 72ed41d37222046f6dfa594aedaa30a0bb38756b
ms.contentlocale: ja-jp
ms.lasthandoff: 05/18/2017

---
# <a name="evaluation-of-tokens"></a>トークンの評価
コンパイラは、トークンを解釈するときに、1 つのトークンにできる限り多くの文字を含めてから、次のトークンに進みます。 このような動作をするため、空白で正しく区切られていない場合、意図したとおりにトークンが解釈されない可能性があります。 次のような式があるとします。  
  
```  
i+++j  
```  
  
 この例では、コンパイラは、3 個のプラス記号から最初に最も長い可能な演算子 (`++`) を取り出し、次に残りの正符号を加算演算子 (`+`) として処理します。 したがって、この式は `(i++) + (j)` ではなく、`(i) + (++j)` として評価されます。 この場合や同様の場合、空白とかっこを使用してあいまいさを回避し、式が適切に評価されるようにします。  
  
 **Microsoft 固有の仕様**  
  
 C コンパイラは Ctrl + Z 文字をファイル終端 (EOF) として扱います。 Ctrl + Z 以降のテキストは無視されます。  
  
 **Microsoft 固有の仕様はここまで**  
  
## <a name="see-also"></a>関連項目  
 [C トークン](../c-language/c-tokens.md)