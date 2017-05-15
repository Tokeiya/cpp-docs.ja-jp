---
title: "コンパイラ エラー C3633 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C3633
dev_langs:
- C++
helpviewer_keywords:
- C3633
ms.assetid: 7d65babf-2191-4d67-a69f-f5c4c2ddf946
caps.latest.revision: 14
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
ms.sourcegitcommit: c243063a9770542f137d5950e8a269f771960f74
ms.openlocfilehash: 76b98ae31e8d8416360415fd5989975533d6fb66
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3633"></a>コンパイラ エラー C3633
'メンバー' をマネージ '型' のメンバーとして定義することはできません。  
  
CLR 参照クラスのデータ メンバーは、POD C++ 以外の型にすることはできません。  POD ネイティブ型は CLR 型にインスタンス化することのみできます。  たとえば、POD 型では、コピー コンス トラクターまたは代入演算子を含めることはできません。  
  
## <a name="example"></a>例  
次の例では、c3633 エラーを生成します。  
  
```  
// C3633.cpp  
// compile with: /clr /c  
#pragma warning( disable : 4368 )  
  
class A1 {  
public:  
   A1() { II = 0; }  
   int II;  
};  
  
ref class B {  
public:  
   A1 a1;   // C3633  
   A1 * a2;   // OK  
   B() : a2( new A1 ) {}  
    ~B() { delete a2; }  
};  
```  
