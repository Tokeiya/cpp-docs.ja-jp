---
title: "コンパイラ エラー C2910 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2910
dev_langs: C++
helpviewer_keywords: C2910
ms.assetid: 09c50e6a-e099-42f6-8ed6-d80e292a7a36
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: db1c4d7b4533d6bbfb0848c1dc16a7336ad81eb0
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2910"></a>コンパイラ エラー C2910
'function': 明示的特殊化できません  
  
 コンパイラでは、明示的に特殊化関数を 2 回の試行が検出されました。  
  
 次の例では、C2910 が生成されます。  
  
```  
// C2910.cpp  
// compile with: /c  
template <class T>  
struct S;  
  
template <> struct S<int> { void f() {} };  
template <> void S<int>::f() {}   // C2910 delete this specialization  
```  
  
 C2910 は、テンプレートでないメンバーを明示的に特殊化しようとする場合にも生成できます。 つまり、関数テンプレートを明示的にのみ特殊化することができます。  
  
 次の例では、C2910 が生成されます。  
  
```  
// C2910b.cpp  
// compile with: /c  
template <class T> struct A {  
   A(T* p);  
};  
  
template <> struct A<void> {  
   A(void* p);  
};  
  
template <class T>  
inline A<T>::A(T* p) {}  
  
template <> A<void>::A(void* p){}   // C2910  
// try the following line instead  
// A<void>::A(void* p){}  
```  
  
 このエラーは Visual Studio .NET 2003 で行われたコンパイラ準拠作業の結果として生成することも: です。  
  
 コードは、Visual Studio .NET 2003 バージョンと Visual Studio .NET バージョンの Visual C では無効になります、削除`template <>`です。  
  
 次の例では、C2910 が生成されます。  
  
```  
// C2910c.cpp  
// compile with: /c  
template <class T> class A {  
   void f();  
};  
  
template <> class A<int> {  
   void f();  
};  
  
template <> void A<int>::f() {}   // C2910  
// try the following line instead  
// void A<int>::f(){}   // OK  
```