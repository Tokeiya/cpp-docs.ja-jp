---
title: "コンパイラ エラー C3484 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3484
dev_langs: C++
helpviewer_keywords: C3484
ms.assetid: 2fe847fa-f6ee-4978-bc1d-b6dc6ae906ac
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 0ec019561a042b5dd5fd05aa8660bc8ff6b1d976
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3484"></a>コンパイラ エラー C3484
戻り値の型の前に '->' が必要です  
  
 ラムダ式の戻り値の型の前に `->` を指定する必要があります。  
  
### <a name="to-correct-this-error"></a>このエラーを解決するには  
  
-   戻り値の型の前に `->` を指定します。  
  
## <a name="example"></a>例  
 次の例では C3484 が生成されます。  
  
```  
// C3484a.cpp  
  
int main()  
{  
   return []() . int { return 42; }(); // C3484  
}  
```  
  
## <a name="example"></a>例  
 次の例では、ラムダ式の戻り値の型の前に `->` を指定して C3484 を解決します。  
  
```  
// C3484b.cpp  
  
int main()  
{  
   return []() -> int { return 42; }();  
}  
```  
  
## <a name="see-also"></a>関連項目  
 [ラムダ式](../../cpp/lambda-expressions-in-cpp.md)