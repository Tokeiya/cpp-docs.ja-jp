---
title: "hash_map::clear (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_map::clear
dev_langs: C++
helpviewer_keywords: clear member [STL/CLR]
ms.assetid: a2782336-f130-4e27-923e-7dd43c542d30
caps.latest.revision: "17"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 27fc4f214a3f96f1821abbac223757f8c7ab5ad5
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="hashmapclear-stlclr"></a>hash_map::clear (STL/CLR)
すべての要素を削除します。  
  
## <a name="syntax"></a>構文  
  
```  
void clear();  
```  
  
## <a name="remarks"></a>コメント  
 このメンバー関数が効果的に呼び出し[hash_map::erase (STL/CLR)](../dotnet/hash-map-erase-stl-clr.md) `(` [hash_map::begin (STL/CLR)](../dotnet/hash-map-begin-stl-clr.md) `(),` [hash_map::end (STL/CLR)](../dotnet/hash-map-end-stl-clr.md)`())`. これを使用するには、被制御シーケンスが空であることを確認します。  
  
## <a name="example"></a>例  
  
```  
// cliext_hash_map_clear.cpp   
// compile with: /clr   
#include <cliext/hash_map>   
  
typedef cliext::hash_map<wchar_t, int> Myhash_map;   
int main()   
    {   
    Myhash_map c1;   
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
    c1.insert(Myhash_map::make_value(L'c', 3));   
  
// display contents " [a 1] [b 2] [c 3]"   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
  
// clear the container and reinspect   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
  
    c1.insert(Myhash_map::make_value(L'a', 1));   
    c1.insert(Myhash_map::make_value(L'b', 2));   
  
// display contents " [a 1] [b 2]"   
    for each (Myhash_map::value_type elem in c1)   
        System::Console::Write(" [{0} {1}]", elem->first, elem->second);   
    System::Console::WriteLine();   
    c1.clear();   
    System::Console::WriteLine("size() = {0}", c1.size());   
    return (0);   
    }  
  
```  
  
```Output  
 [a 1] [b 2] [c 3]  
size() = 0  
 [a 1] [b 2]  
size() = 0  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext/hash_map >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [hash_map (STL/CLR)](../dotnet/hash-map-stl-clr.md)   
 [hash_map::erase (STL/CLR)](../dotnet/hash-map-erase-stl-clr.md)