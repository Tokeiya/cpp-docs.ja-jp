---
title: "コンパイラの警告 (レベル 1) C4546 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4546
dev_langs: C++
helpviewer_keywords: C4546
ms.assetid: 071e1709-3841-46c1-8e71-96109cd22041
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: a9b424c640f889f694f002c35033afd4a611396e
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-level-1-c4546"></a>コンパイラの警告 (レベル 1) C4546
コンマの前の関数呼び出しに引数一覧がありません。  
  
 正しい形式でコンマ式が検出されました。  
  
 既定では、この警告はオフに設定されています。 詳細については、「 [Compiler Warnings That Are Off by Default](../../preprocessor/compiler-warnings-that-are-off-by-default.md)」を参照してください。  
  
## <a name="example"></a>例  
 次の例では、C4546 が生成されます。  
  
```  
// C4546.cpp  
// compile with: /W1  
#pragma warning (default : 4546)  
void f(int i) {  
   i++;  
}  
  
int main() {  
   int i = 0, k = 0;  
  
   if ( f, k )   // C4546  
   // try the following line instead  
   // if ( f(i), k )  
      i++;  
}  
```