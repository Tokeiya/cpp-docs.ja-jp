---
title: "コンパイラ エラー C2438 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2438
dev_langs:
- C++
helpviewer_keywords:
- C2438
ms.assetid: 3a0ab3ba-d0e4-4d8f-971d-e503397cc827
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 1771d3c6c241db6430eaa66fece5562a3bc1349a
ms.contentlocale: ja-jp
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2438"></a>コンパイラ エラー C2438
'identifier': コンス トラクターを使用して静的クラスのデータを初期化できません  
  
 コンス トラクターを使用して、クラスの静的メンバーを初期化します。 クラス宣言の外側の定義では、静的メンバーを初期化する必要があります。  
  
 次の例では、C2438 が生成されます。  
  
```  
// C2438.cpp  
struct X {  
   X(int i) : j(i) {}   // C2438  
   static int j;  
};  
  
int X::j;  
  
int main() {  
   X::j = 1;  
}  
```
