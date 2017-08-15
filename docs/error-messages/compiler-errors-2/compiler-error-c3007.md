---
title: "コンパイラ エラー C3007 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3007
dev_langs:
- C++
helpviewer_keywords:
- C3007
ms.assetid: e415ef42-bdc9-4f32-8198-5e25b289a089
caps.latest.revision: 6
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
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 7e4ffbea182349faeb827799e31863fdbdd42d75
ms.contentlocale: ja-jp
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3007"></a>コンパイラ エラー C3007
'arg' : OpenMP 'directive' ディレクティブ上の句には、引数を指定できません  
  
 OpenMP ディレクティブに引数が含まれていましたが、このディレクティブは引数を取りません。  
  
 次の例では C3007 が生成されます。  
  
```  
// C3007.c  
// compile with: /openmp  
int main()  
{  
   #pragma omp parallel for ordered(2)   // C3007  
}  
```