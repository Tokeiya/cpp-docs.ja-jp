---
title: "コンパイラ エラー C3018 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3018
dev_langs:
- C++
helpviewer_keywords:
- C3018
ms.assetid: 685be45f-f116-43a8-a88d-05ab6616e2f1
caps.latest.revision: 7
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
ms.openlocfilehash: d4e93e6f9b268b16350ee8cda6b55f7c0f140985
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3018"></a>コンパイラ エラー C3018
'var1' : OpenMP 'for' テストまたはインクリメントは、インデックス変数 'var2' を使用しなければなりません  
  
 OpenMP ステートメント内の `for` ループは、インデックスに使用するときのように、テストとインクリメントに同じ変数を使用する必要があります。  
  
 次の例では C3018 が生成されます。  
  
```  
// C3018.cpp  
// compile with: /openmp  
int main()  
{  
   int i = 0, j = 5;  
  
   #pragma omp parallel  
   {  
      #pragma omp for  
      for (i = 0; j < 10; ++i)   // C3018  
      // try the the following line instead  
      // for (i = 0; i < 10; ++i)  
         j *= 2;  
  
      #pragma omp for  
      for (i = 0; i < 10; j = j + i)   // C3018  
      // try the the following line instead  
      // for (i = 0; i < 10; i = j + i)  
         j *= 2;  
   }  
}  
```