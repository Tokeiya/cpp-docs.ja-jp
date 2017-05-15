---
title: "コンパイラ エラー C2046 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2046
dev_langs:
- C++
helpviewer_keywords:
- C2046
ms.assetid: f0c8f9dd-dbd7-4c4a-8838-fde54208ec71
caps.latest.revision: 8
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
ms.openlocfilehash: 2c68f3e67fff8353fe5e4ca9881532343180a8e1
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2046"></a>コンパイラ エラー C2046
'case' が正しくありません。  
  
 キーワード `case` は `switch` ステートメントでのみ使用できます。  
  
 次の例では C2046 エラーが生成されます。  
  
```  
// C2046.cpp  
int main() {  
   case 0:   // C2046  
}  
```  
  
 考えられる解決策:  
  
```  
// C2046b.cpp  
int main() {  
   int i = 0;  
  
   switch(i) {  
      case 0:  
      break;  
  
      default:  
      break;  
   }  
}  
```