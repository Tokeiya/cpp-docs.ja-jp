---
title: "コンパイラ エラー C3798 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C3798"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3798"
ms.assetid: b2f8b1d8-8812-49b8-a346-28e48f02ba5c
caps.latest.revision: 4
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 4
---
# コンパイラ エラー C3798
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'指定子': プロパティ宣言は、オーバーライド指定子を含むことはできません。プロパティの get または set メソッドに配置しなければなりません  
  
 プロパティの宣言が正しくありません。  詳細については、次のトピックを参照してください  
  
-   [property](../../windows/property-cpp-component-extensions.md)  
  
-   [abstract](../../windows/abstract-cpp-component-extensions.md)  
  
-   [sealed](../../windows/sealed-cpp-component-extensions.md)  
  
## 使用例  
 次の例では C3798 エラーが生成されます。  
  
```  
// C3798.cpp  
// compile with: /clr /c  
ref struct A {  
   property int Prop_1 abstract;   // C3798  
   property int Prop_2 sealed;   // C3798  
  
   // OK  
   property int Prop_3 {  
      virtual int get() abstract;  
      virtual void set(int i) abstract;  
   }  
  
   property int Prop_4 {  
      virtual int get() sealed;  
      virtual void set(int i) sealed;  
   }  
};  
```