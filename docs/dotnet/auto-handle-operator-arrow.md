---
title: "auto_handle::operator-&gt; | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "msclr::auto_handle::operator->"
  - "auto_handle.operator->"
  - "auto_handle::operator->"
  - "msclr.auto_handle.operator->"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "auto_handle::operator->"
ms.assetid: c8c7a771-ea15-41fa-981a-065b8d1162b4
caps.latest.revision: 10
caps.handback.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# auto_handle::operator-&gt;
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

メンバー アクセス演算子。  
  
## 構文  
  
```  
_element_type ^ operator->();  
```  
  
## 戻り値  
 `auto_handle` によりラップされるオブジェクト。  
  
## 使用例  
  
```  
// msl_auto_handle_op_arrow.cpp  
// compile with: /clr  
#include <msclr\auto_handle.h>  
  
using namespace System;  
using namespace msclr;  
  
ref class ClassA {  
protected:     
   String^ m_s;  
public:  
   ClassA( String^ s ) : m_s( s ) {}  
  
   virtual void PrintHello() {  
      Console::WriteLine( "Hello from {0} A!", m_s );  
   }  
  
   int m_i;  
};  
  
int main() {  
   auto_handle<ClassA> a( gcnew ClassA( "first" ) );  
   a->PrintHello();  
  
   a->m_i = 5;  
   Console::WriteLine( "a->m_i = {0}", a->m_i );  
}  
```  
  
  **Hello 最初に A ~\!**  
**次の\>\_i \= 5**   
## 必要条件  
 **ヘッダー ファイル** \<msclr\\auto\_handle.h\>  
  
 **名前空間** の msclr  
  
## 参照  
 [auto\_handle Members](../dotnet/auto-handle-members.md)   
 [auto\_handle::get](../dotnet/auto-handle-get.md)