---
title: "コンパイラ エラー C3037 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3037
dev_langs: C++
helpviewer_keywords: C3037
ms.assetid: 9ba8a890-d3c7-4cce-93c5-d358e2bfad28
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 7fc59984a3fb47d9dd00d479e771fd11f6bab242
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3037"></a>コンパイラ エラー C3037
'var': 'reduction' 句の変数は、それを囲むコンテキスト内で共有されなければなりません  
  
 [reduction](../../parallel/openmp/reference/reduction.md) 句で指定される変数は、コンテキスト内の各スレッドに対してプライベートにすることはできません。  
  
 次の例では C3037 が生成されます。  
  
```  
// C3037.cpp  
// compile with: /openmp /c  
int g_i;  
  
int main() {  
   int i;  
  
   #pragma omp parallel private(g_i)  
   // try the following line instead  
   // #pragma omp parallel   
   {  
      #pragma omp for reduction(+:g_i)   // C3037  
      for (i = 0 ; i < 10 ; ++i) {  
         g_i += i;  
      }  
   }  
}  
```