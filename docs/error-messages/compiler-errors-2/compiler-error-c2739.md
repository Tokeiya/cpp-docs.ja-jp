---
title: "コンパイラ エラー C2739 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2739
dev_langs: C++
helpviewer_keywords: C2739
ms.assetid: 5b63e435-7631-43d7-805e-f2adefb7e517
caps.latest.revision: "11"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: b6d2647fe6addc8f5c68ef70b91a244782f467a4
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2739"></a>コンパイラ エラー C2739
'number': 明示的なマネージまたは WinRT 配列の次元は 1 から 32 の間でなければなりません  
  
 配列の次元が 1 ～ 32 ではありませんでした。  
  
 次の例では、C2739 を生成し、その修正方法を示しています。  
  
```  
// C2739.cpp  
// compile with: /clr  
int main() {  
   array<int, -1>^a;   // C2739  
   // try the following line instead  
   // array<int, 2>^a;  
}  
```