---
title: "コンパイラ エラー C3748 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3748
dev_langs: C++
helpviewer_keywords: C3748
ms.assetid: 6fe71a0a-dd93-4ce6-9729-b9616360cf34
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 678fdb112114e7e6fa8aff148af488a17952fa47
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3748"></a>コンパイラ エラー C3748
'interface': マネージ インターフェイスはイベントを発生させる可能性がありますいません。  
  
 [_ _Event](../../cpp/event.md)インターフェイス内のキーワードが出現ことはできません。  
  
 次の例では、C3748 が生成されます。  
  
```  
// C3748.cpp  
__interface I {  
// try the following line instead  
// struct I {  
   __event void f();   // C3748  
};  
  
int main() {  
}  
```