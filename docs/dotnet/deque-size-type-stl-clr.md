---
title: "deque::size_type (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::deque::size_type
dev_langs: C++
helpviewer_keywords: size_type member [STL/CLR]
ms.assetid: c598871c-0ce8-4599-ab4c-2d0ea5f3f8e4
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 36b307e371fea279a8a3931221ee2cb05e9aa834
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="dequesizetype-stlclr"></a>deque::size_type (STL/CLR)
2 つの要素の間の距離を符号付きの型。  
  
## <a name="syntax"></a>構文  
  
```  
typedef int size_type;  
```  
  
## <a name="remarks"></a>コメント  
 この型は、負でない要素の数を表します。  
  
## <a name="example"></a>例  
  
```  
// cliext_deque_size_type.cpp   
// compile with: /clr   
#include <cliext/deque>   
  
int main()   
    {   
    cliext::deque<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// compute positive difference   
    cliext::deque<wchar_t>::size_type diff = c1.end() - c1.begin();   
    System::Console::WriteLine("end()-begin() = {0}", diff);   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
end()-begin() = 3  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext/deque >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [deque (STL/CLR)](../dotnet/deque-stl-clr.md)   
 [deque::empty (STL/CLR)](../dotnet/deque-empty-stl-clr.md)