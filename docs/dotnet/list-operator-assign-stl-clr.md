---
title: "list::operator = (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::list::operator=
dev_langs: C++
helpviewer_keywords: operator= member [STL/CLR]
ms.assetid: 0e4fdcc6-7574-40af-b947-98c2c683676d
caps.latest.revision: "14"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: a308c3af69d3a83a5a9a1ec461e1b086abbaa7fe
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="listoperator-stlclr"></a>list::operator= (STL/CLR)
被制御シーケンスを置き換えます。  
  
## <a name="syntax"></a>構文  
  
```  
list<Value>% operator=(list<Value>% right);  
```  
  
#### <a name="parameters"></a>パラメーター  
 右  
 コピーするコンテナー。  
  
## <a name="remarks"></a>コメント  
 メンバー演算子コピー`right`オブジェクトを返します`*this`です。 これを使用して、被制御シーケンスを `right` の被制御シーケンスのコピーと置き換えます。  
  
## <a name="example"></a>例  
  
```  
// cliext_list_operator_as.cpp   
// compile with: /clr   
#include <cliext/list>   
  
int main()   
    {   
    cliext::list<wchar_t> c1;   
    c1.push_back(L'a');   
    c1.push_back(L'b');   
    c1.push_back(L'c');   
  
// display contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// assign to a new container   
    cliext::list<wchar_t> c2;   
    c2 = c1;   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
a b c  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext/一覧 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [一覧 (STL/CLR)](../dotnet/list-stl-clr.md)   
 [list::assign (STL/CLR)](../dotnet/list-assign-stl-clr.md)