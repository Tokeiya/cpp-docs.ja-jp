---
title: "コンパイラ エラー C2149 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2149
dev_langs:
- C++
helpviewer_keywords:
- C2149
ms.assetid: 7a106dab-d79f-41b9-85be-f36e86e4d2ab
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
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 6c1b6422ae01f77729fba3a4d6c39df0257a9c8c
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2149"></a>コンパイラ エラー C2149
'identifier': 名前付きビットフィールドの幅が&0; です  
  
 名前を指定しない場合にのみ、ビット フィールドの幅を&0; にできます。  
  
 次の例では C2149 が生成されます。  
  
```  
// C2149.cpp  
// compile with: /c  
struct C {  
   int i : 0;   // C2149  
   int j : 2;   // OK  
};  
```