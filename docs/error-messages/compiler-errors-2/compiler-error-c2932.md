---
title: "コンパイラ エラー C2932 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2932
dev_langs: C++
helpviewer_keywords: C2932
ms.assetid: c28e88d9-e654-4367-bfb4-13c780bca9bd
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 49565a60a6623e80b1d367bf3d341cfe60b639af
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2932"></a>コンパイラ エラー C2932
'class': type-class-id が 'identifier' のデータ メンバーとして再定義されています  
  
 ジェネリック クラスまたはテンプレート クラスをデータ メンバーとして使用することはできません。  
  
 次の例では C2932 が生成されます。  
  
```  
// C2932.cpp  
// compile with: /c  
template<class T>   
struct TC {};   
  
struct MyStruct {  
   int TC<int>;   // C2932  
   int TC;   // OK  
};  
```  
  
 C2932 は、ジェネリックを使用しているときにも発生することがあります。  
  
```  
// C2932b.cpp  
// compile with: /clr /c  
generic<class T>  
ref struct GC {};  
  
struct MyStruct {  
   int GC<int>;   // C2932  
   int GC;   // OK  
};  
```