---
title: "コンパイラ エラー C2159 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2159
dev_langs:
- C++
helpviewer_keywords:
- C2159
ms.assetid: 925a2cbd-43c9-45ee-a373-84004350b380
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
ms.openlocfilehash: 0865464dec30bb5cefa53838c1fceb07b8b60616
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2159"></a>コンパイラ エラー C2159
2 つ以上のストレージ クラスが指定されています。  
  
 宣言に複数のストレージ クラスが含まれています。  
  
 次の例では C2159 が生成されます。  
  
```  
// C2159.cpp  
// compile with: /c  
static int i;   // OK  
extern static int i;   // C2159  
```