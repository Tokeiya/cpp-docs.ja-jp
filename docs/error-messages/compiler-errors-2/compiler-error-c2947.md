---
title: "コンパイラ エラー C2947 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2947
dev_langs:
- C++
helpviewer_keywords:
- C2947
ms.assetid: 6c056f62-ec90-4883-8a67-aeeb6ec13546
caps.latest.revision: 10
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: bb5b22d4fd4b874e19cff564dec96609f9da0789
ms.contentlocale: ja-jp
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2947"></a>コンパイラ エラー C2947
指定してください ' >' を構造を終了するには、'構文' が見つかりました  
  
 ジェネリックまたはテンプレートの引数リストが正しく終了がいないことがあります。  
  
 C2947 は、構文エラーによっても生成できます。  
  
 次の例では、C2947 が生成されます。  
  
```  
// C2947.cpp  
// compile with: /c  
template <typename T>=   // C2947  
// try the following line instead  
// template <typename T>  
struct A {};  
```
