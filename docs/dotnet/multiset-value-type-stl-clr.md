---
title: "multiset::value_type (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::multiset::value_type
dev_langs: C++
helpviewer_keywords: value_type member [STL/CLR]
ms.assetid: 6a88ee7a-27a1-4fbb-a56c-9c8d7abc4471
caps.latest.revision: "14"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: a84c316232dfe12f89c6fcbac6a4933654a5072d
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="multisetvaluetype-stlclr"></a>multiset::value_type (STL/CLR)
要素の型。  
  
## <a name="syntax"></a>構文  
  
```  
typedef generic_value value_type;  
```  
  
## <a name="remarks"></a>コメント  
 この型は `generic_value` の同意語です。  
  
## <a name="example"></a>例  
  
```  
// cliext_multiset_value_type.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::multiset<wchar_t> Mymultiset;   
int main()   
    {   
    Mymultiset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display contents " a b c" using value_type   
    for (Mymultiset::iterator it = c1.begin(); it != c1.end(); ++it)   
        {   // store element in value_type object   
        Mymultiset::value_type val = *it;   
  
        System::Console::Write(" {0}", val);   
        }   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext と set >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [マルチセット (STL/CLR)](../dotnet/multiset-stl-clr.md)   
 [multiset::const_reference (STL/CLR)](../dotnet/multiset-const-reference-stl-clr.md)   
 [multiset::key_type (STL/CLR)](../dotnet/multiset-key-type-stl-clr.md)   
 [multiset::reference (STL/CLR)](../dotnet/multiset-reference-stl-clr.md)