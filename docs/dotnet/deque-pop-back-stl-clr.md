---
title: "deque::pop_back (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "reference"
f1_keywords: 
  - "cliext::deque::pop_back"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "pop_back メンバー [STL/CLR]"
ms.assetid: 528d2c89-104c-45f7-8f05-41fe217ee37c
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 14
---
# deque::pop_back (STL/CLR)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

最後の要素を削除します。  
  
## 構文  
  
```  
void pop_back();  
```  
  
## 解説  
 メンバー関数は空でない必要があります。被制御シーケンスの最後の要素を削除します。  戻るに 1 個の要素で deque を短くするために使用します。  
  
## 使用例  
  
```  
// cliext_deque_pop_back.cpp   
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
  
// pop an element and redisplay   
    c1.pop_back();   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
  **b c**  
 **b**   
## 必要条件  
 **ヘッダー:** \<cliext\/deque\>  
  
 **名前空間:** の cliext  
  
## 参照  
 [deque](../dotnet/deque-stl-clr.md)   
 [deque::pop\_front](../dotnet/deque-pop-front-stl-clr.md)   
 [deque::push\_back](../dotnet/deque-push-back-stl-clr.md)   
 [deque::push\_front](../dotnet/deque-push-front-stl-clr.md)