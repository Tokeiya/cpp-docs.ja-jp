---
title: "コンパイラの警告 (レベル 1) C4374 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4374"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4374"
ms.assetid: 4ac9aaec-d815-4b6e-825f-fa872092dd3b
caps.latest.revision: 11
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 11
---
# コンパイラの警告 (レベル 1) C4374
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'function1': インターフェイス メソッドは、仮想でないメソッド 'function2' によって実装されません。  
  
 コンパイラはメソッド定義の [virtual](../../cpp/virtual-specifier.md) キーワードを探しましたが、見つかりませんでした。  
  
 次の例では警告 C4374 が生成されます。  
  
```  
// C4374.cpp  
// compile with: /clr /W1 /c /WX  
public interface class I {  
   void f();  
};  
  
public ref struct B {  
   void f() {  
      System::Console::WriteLine("B::f()");  
   }  
};  
  
public ref struct C {  
   virtual void f() {  
      System::Console::WriteLine("C::f()");  
   }  
};  
  
public ref struct D : B, I {};   // C4374  
public ref struct E : C, I {};   // OK  
```