---
title: "operator&gt; (deque) (STL/CLR) | Microsoft Docs"
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
  - "cliext::deque::operator>"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "operator> メンバー [STL/CLR]"
ms.assetid: b207be0a-c6d8-4d70-8b8d-beb48e859441
caps.latest.revision: 17
caps.handback.revision: 15
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# operator&gt; (deque) (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

比較 Deque より大きい。  
  
## 構文  
  
```  
template<typename Value>  
    bool operator>(deque<Value>% left,  
        deque<Value>% right);  
```  
  
#### パラメーター  
 \[left\]  
 比較の左辺のコンテナー。  
  
 \[right\]  
 比較の右辺のコンテナー。  
  
## 解説  
 演算子関数の戻り値 `right``<``left`。  2 個の deques が要素によって比較された要素の場合 `left` が `right` の後に並べるかをテストするときに使用します。  
  
## 使用例  
  
```  
// cliext_deque_operator_gt.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    cliext::deque<wchar_t> c2;   
    c2.push_back(L'a');   
    c2.push_back(L'b');   
    c2.push_back(L'd');   
  
// display contents " a b d"   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("[a b c] > [a b c] is {0}",   
        c1 > c1);   
    System::Console::WriteLine("[a b d] > [a b c] is {0}",   
        c2 > c1);   
    return (0);   
    }  
  
```  
  
  **b c**  
 **b d**  
**b c \[\] \> \[\] b c false です。**  
**\[\] \> b c d b \[\]当てはまります。**   
## 必要条件  
 **ヘッダー:** \<cliext\/deque\>  
  
 **名前空間:** の cliext  
  
## 参照  
 [deque](../dotnet/deque-stl-clr.md)   
 [operator\=\= \(deque\)](../dotnet/operator-equality-deque-stl-clr.md)   
 [deque::operator\!\=](../dotnet/deque-operator-inequality-stl-clr.md)   
 [operator\< \(deque\)](../dotnet/operator-less-than-deque-stl-clr.md)   
 [operator\>\= \(deque\)](../dotnet/operator-greater-or-equal-deque-stl-clr.md)   
 [operator\<\= \(deque\)](../dotnet/operator-less-or-equal-deque-stl-clr.md)