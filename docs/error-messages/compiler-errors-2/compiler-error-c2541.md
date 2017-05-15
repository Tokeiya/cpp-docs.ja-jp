---
title: "コンパイラ エラー C2541 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2541"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2541"
ms.assetid: ed95180f-00df-4e62-a8e9-1b6dab8281bf
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# コンパイラ エラー C2541
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'delete' : ポインターではないオブジェクトを削除することはできません。  
  
 [delete](../../cpp/delete-operator-cpp.md) 演算子が、ポインターではないオブジェクトに使用されています。  
  
 次の例では警告 C2541 が生成されます。  
  
```  
// C2541.cpp  
int main() {  
   int i;  
   delete i;   // C2541 i not a pointer  
  
   // OK  
   int *ip = new int;  
   delete ip;  
}  
```