---
title: "コンパイラの警告 (レベル 1) C4172 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4172"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4172"
ms.assetid: a8d2bf65-d8b1-4fe3-8340-a223d7e7fde6
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# コンパイラの警告 (レベル 1) C4172
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

ローカル変数またはテンポラリのアドレスを返します。  
  
 関数がローカル変数または一時オブジェクトのアドレスを返しています。  ローカル変数と一時オブジェクトは、関数から戻るときに破棄されるため、返されるアドレスは無効です。  
  
 関数のデザインを変更して、ローカル オブジェクトのアドレスを返さないようにします。  
  
 次の例では警告 C4172 が生成されます。  
  
```  
// C4172.cpp  
// compile with: /W1 /LD  
float f = 10;  
  
const double& bar() {  
// try the following line instead  
// const float& bar() {  
   return f;   // C4172  
}  
```