---
title: "コンパイラ エラー C2802 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2802
dev_langs:
- C++
helpviewer_keywords:
- C2802
ms.assetid: 08b68c0e-9382-40ac-8949-39a7a2749e05
caps.latest.revision: 8
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
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 031c5b75a0f4008196501b8fb798384a52bbdf77
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2802"></a>コンパイラ エラー C2802
静的メンバー '演算子' には、正式なパラメーターがありません。  
  
 によって、演算子が宣言された、`static`メンバー関数には、少なくとも&1; つのパラメーターを持つ必要があります。  
  
 次の例では、c2802 エラーが生成されます。  
  
```  
// C2802.cpp  
// compile with: /clr /c  
ref class A {  
   static operator+ ();   // C2802  
   static operator+ (A^, A^);   // OK  
};  
```