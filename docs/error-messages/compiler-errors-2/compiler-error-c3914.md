---
title: "コンパイラ エラー C3914 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3914
dev_langs: C++
helpviewer_keywords: C3914
ms.assetid: 8f3190e6-ee50-4916-9ecc-3b8748b2e1e7
caps.latest.revision: "5"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 4d38483d3edd477babb7a240a7b79841850f6a9e
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3914"></a>コンパイラ エラー C3914
既定のプロパティを静的にすることはできません。  
  
既定のプロパティの宣言が正しくありません。  詳細については、次を参照してください。[する方法: プロパティを使用して C + + CLI](../../dotnet/how-to-use-properties-in-cpp-cli.md)です。  
  
## <a name="example"></a>例  
次の例では、C3914 を生成し、その修正方法を示しています。  
  
```  
// C3914.cpp  
// compile with: /clr /c  
ref struct X {  
   static property int default[int] {   // C3914  
   // try the following line instead  
   // property int default[int] {  
      int get(int) { return 0; }  
      void set(int, int) {}  
   }  
};  
```