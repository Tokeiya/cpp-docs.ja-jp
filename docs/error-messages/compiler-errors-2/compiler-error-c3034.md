---
title: "コンパイラ エラー C3034 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3034
dev_langs:
- C++
helpviewer_keywords:
- C3034
ms.assetid: 49db8bac-2720-4622-94e3-7988f1603fa3
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
ms.openlocfilehash: 5dd1c4a4236b5fe37824b354b5645679d533b03f
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3034"></a>コンパイラ エラー C3034
OpenMP 'directive1' ディレクティブを、'directive2' ディレクティブの中に直接入れ子にすることはできません  
  
 一部のディレクティブは入れ子にできません。 このエラーを修正するには、1 つのディレクティブのブロックに両方のディレクティブのステートメントをマージするか、または連続するディレクティブを作成します。  
  
 次の例では C3034 が生成されます。  
  
```  
// C3034.cpp  
// compile with: /openmp /link vcomps.lib  
int main() {  
  
   #pragma omp single  
   {  
      #pragma omp single   // C3034   
      {  
      ;  
      }  
   }  
  
   // Two consecutive single clauses are OK.  
   #pragma omp single  
   {  
   }  
  
   #pragma omp single  
   {  
   }  
}  
```