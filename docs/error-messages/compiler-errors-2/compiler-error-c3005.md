---
title: "コンパイラ エラー C3005 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3005
dev_langs:
- C++
helpviewer_keywords:
- C3005
ms.assetid: 30bad565-e79f-4c3f-82cb-a74bd0baab8f
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
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 37df53e1e47d25a563ece741dc1130d0f79b350d
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3005"></a>コンパイラ エラー C3005
'error_text' : OpenMP 'directive' ディレクティブでは予期しないトークンです  
  
 OpenMP ディレクティブの形式が正しくありません。  
  
 次の例では C3005 が生成されます。  
  
```  
// C3005.c  
// compile with: /openmp  
int main()  
{  
   #pragma omp parallel + for   // C3005  
}  
```  
  
 プラグマと同じ行で始め中かっこを使用した場合も、C3005 が発生します。  
  
```  
// C3005b.c  
// compile with: /openmp  
int main() {  
   #pragma omp parallel {   // C3005 put open brace on next line  
   lbl2:;  
   }  
   goto lbl2;  
}  
```