---
title: "hash_set::lower_bound (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_set::lower_bound
dev_langs: C++
helpviewer_keywords: lower_bound member [STL/CLR]
ms.assetid: 54fe8ee5-1977-4192-9cc6-b51e84b03a16
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: ee6c0cbea5a6e4b2d4730de7bb55564bb8200e85
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="hashsetlowerbound-stlclr"></a>hash_set::lower_bound (STL/CLR)
指定したキーに一致する範囲の先頭を検出します。  
  
## <a name="syntax"></a>構文  
  
```  
iterator lower_bound(key_type key);  
```  
  
#### <a name="parameters"></a>パラメーター  
 key  
 検索対象のキー値。  
  
## <a name="remarks"></a>コメント  
 このメンバー関数は、最初の要素を決定する`X`同じバケットにハッシュされる被制御シーケンス内`key`と同じ順序が`key`です。 このような要素が存在しないかどうかが返されます[hash_set::end (STL/CLR)](../dotnet/hash-set-end-stl-clr.md)`()`; 指定する反復子を返しますそれ以外の場合`X`です。 これを使用して、指定したキーと一致する、被制御シーケンス内で現在の要素のシーケンスの先頭を検索します。  
  
## <a name="example"></a>例  
  
```  
// cliext_hash_set_lower_bound.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_set<wchar_t> Myhash_set;   
int main()   
    {   
    Myhash_set c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("lower_bound(L'x')==end() = {0}",   
        c1.lower_bound(L'x') == c1.end());   
  
    System::Console::WriteLine("*lower_bound(L'a') = {0}",   
        *c1.lower_bound(L'a'));   
    System::Console::WriteLine("*lower_bound(L'b') = {0}",   
        *c1.lower_bound(L'b'));   
    return (0);   
    }  
  
```  
  
```Output  
 a b c  
lower_bound(L'x')==end() = True  
*lower_bound(L'a') = a  
*lower_bound(L'b') = b  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext/hash_set >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [hash_set (STL/CLR)](../dotnet/hash-set-stl-clr.md)   
 [hash_set::count (STL/CLR)](../dotnet/hash-set-count-stl-clr.md)   
 [hash_set::equal_range (STL/CLR)](../dotnet/hash-set-equal-range-stl-clr.md)   
 [hash_set::find (STL/CLR)](../dotnet/hash-set-find-stl-clr.md)   
 [hash_set::upper_bound (STL/CLR)](../dotnet/hash-set-upper-bound-stl-clr.md)