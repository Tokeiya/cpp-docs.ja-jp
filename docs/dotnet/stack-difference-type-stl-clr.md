---
title: "stack::difference_type (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::stack::difference_type"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "difference_type メンバー [STL/CLR]"
ms.assetid: 953a0d2a-873c-41e7-b792-15cf18e7a5b4
caps.latest.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 13
---
# stack::difference_type (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

2 個の要素間の符号付きな間隔の種類。  
  
## 構文  
  
```  
typedef int difference_type;  
```  
  
## 解説  
 型は、負のな要素数を表します。  
  
## 使用例  
  
```  
// cliext_stack_difference_type.cpp   
// compile with: /clr   
#include <cliext/stack>   
  
typedef cliext::stack<wchar_t> Mystack;   
int main()   
    {   
    Mystack c1;   
    c1.push(L'a');   
    c1.push(L'b');   
    c1.push(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1.get_container())   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// compute negative difference   
    Mystack::difference_type diff = c1.size();   
    c1.push(L'd');   
    c1.push(L'e');   
    diff -= c1.size();   
    System::Console::WriteLine("pushing 2 = {0}", diff);   
  
// compute positive difference   
    diff = c1.size();   
    c1.pop();   
    c1.pop();   
    c1.pop();   
    diff -= c1.size();   
    System::Console::WriteLine("popping 3 = {0}", diff);   
    return (0);   
    }  
  
```  
  
  **b c**  
**2 つ \= \-2 キーを押す**  
**3 つ \= 3 をポップされます。**   
## 必要条件  
 **ヘッダー:** \<cliext とスタック\>  
  
 **名前空間:** の cliext  
  
## 参照  
 [スタック](../dotnet/stack-stl-clr.md)   
 [stack::size\_type](../dotnet/stack-size-type-stl-clr.md)