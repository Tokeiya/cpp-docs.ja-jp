---
title: "hash_set::const_iterator (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_set::const_iterator
dev_langs: C++
helpviewer_keywords: const_iterator member [STL/CLR]
ms.assetid: 5b346a3e-cdbb-4300-9b25-a16a5f74f9b2
caps.latest.revision: "13"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 0a4dde55c1e019c89565f236d729a55997311cfd
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="hashsetconstiterator-stlclr"></a>hash_set::const_iterator (STL/CLR)
被制御シーケンスの定数反復子の型です。  
  
## <a name="syntax"></a>構文  
  
```  
typedef T2 const_iterator;  
```  
  
## <a name="remarks"></a>コメント  
 この型が指定されていない型のオブジェクトを表します`T2`被制御シーケンスの定数の双方向反復子として使用されることができます。  
  
## <a name="example"></a>例  
  
```  
// cliext_hash_set_const_iterator.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display contents " a b c"   
    Myhash_set::const_iterator cit = c1.begin();   
    for (; cit != c1.end(); ++cit)   
        System::Console::Write(" {0}", *cit);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext/hash_set >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [hash_set (STL/CLR)](../dotnet/hash-set-stl-clr.md)   
 [hash_set::iterator (STL/CLR)](../dotnet/hash-set-iterator-stl-clr.md)