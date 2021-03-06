---
title: "コンパイラ エラー C3538 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3538
dev_langs:
- C++
helpviewer_keywords:
- C3538
ms.assetid: ef3698a5-7356-4c62-b9af-5d3a4baed958
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: da21036ddd4cc8b468f291079e0c475ca1b7c4b3
ms.contentlocale: ja-jp
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c3538"></a>コンパイラ エラー C3538
宣言リストでは 'auto' は常に同じ型に推測される必要があります  
  
 宣言リスト内で宣言されているすべての変数が、同じ型に解決されません。  
  
### <a name="to-correct-this-error"></a>このエラーを解決するには  
  
1.  リスト内のすべての `auto` 宣言が同じ型を推測していることを確認します。  
  
## <a name="example"></a>例  
 次のステートメントは C3538 を生成します。 各ステートメントは複数の変数を宣言していますが、それぞれの 　`auto` キーワードの使用が同じ型を推測していません。  
  
```  
// C3538.cpp  
// Compile with /Zc:auto  
// C3538 expected  
int main()  
{  
// Variable x1 is a pointer to char, but y1 is a double.  
   auto * x1 = "a", y1 = 3.14;    
// Variable c is a char and c1 is char*, but c2, and c3 are pointers to pointers.  
   auto c = 'a', *c1 = &c, * c2 = &c1, * c3 = &c2;   
// Variable x2 is an int, but y2 is a double and z is a char.  
   auto x2(1), y2(0.0), z = 'a';   
// Variable a is a pointer to int, but b is a pointer to double.  
   auto *a = new auto(1), *b = new auto(2.0);   
   return 0;  
}  
```  
  
## <a name="see-also"></a>関連項目  
 [auto キーワード](../../cpp/auto-keyword.md)
