---
title: "コンパイラ エラー C2674 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2674
dev_langs:
- C++
helpviewer_keywords:
- C2674
ms.assetid: 7cbd70d8-d992-44d7-a5cb-dd8cf9c759d2
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 95a136660a660843a13685b822c1e65c4f4259ea
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2674"></a>コンパイラ エラー C2674
ジェネリック宣言はこのコンテキストでは使用できません  
  
 ジェネリック型の宣言が正しくありません。 詳細については、次を参照してください。[ジェネリック](../../windows/generics-cpp-component-extensions.md)します。  
  
## <a name="example"></a>例  
 次の例では、c2674 エラーを生成します。  
  
```  
// C2674.cpp  
// compile with: /clr /c  
void F(generic <class T> ref class R1);   // C2674  
generic <class T> ref class R2 {};   // OK  
```