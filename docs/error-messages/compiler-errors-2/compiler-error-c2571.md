---
title: "コンパイラ エラー C2571 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2571
dev_langs: C++
helpviewer_keywords: C2571
ms.assetid: c6522616-dee9-4d7d-9bf8-30a7e1deaadf
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 8bfb4f9af849efea2fa3aa8a84a57f1cfb4cd502
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2571"></a>コンパイラ エラー C2571
'function': 仮想関数は、'union' 共用体にすることはできません  
  
 仮想関数を持つ共用体が宣言されています。 クラスまたは構造体でのみ仮想関数を宣言することができます。  考えられる解決策:  
  
1.  クラスまたは構造体、共用体を変更します。  
  
2.  非仮想関数を作成します。  
  
 次の例では、C2571 が生成されます。  
  
```  
// C2571.cpp  
// compile with: /c  
union A {  
   virtual void func1();   // C2571  
   void func2();   // OK  
};  
```