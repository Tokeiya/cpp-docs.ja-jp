---
title: "hash_multiset::hash_delegate (STL/CLR) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: cliext::hash_multiset::hash_delegate
dev_langs: C++
helpviewer_keywords: hash_delegate member [STL/CLR]
ms.assetid: 61ccfdfb-6a3c-40aa-902f-49e004a31a75
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: f92bce6ea3bf0cafc1b14def19505d191cc3a185
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="hashmultisethashdelegate-stlclr"></a>hash_multiset::hash_delegate (STL/CLR)
指定したキーに一致する要素を検索します。  
  
## <a name="syntax"></a>構文  
  
```  
hasher^ hash_delegate();  
```  
  
## <a name="remarks"></a>コメント  
 このメンバー関数では、キーの値を整数に変換するために使用されるデリゲートを返します。 キーのハッシュに使用するとします。  
  
## <a name="example"></a>例  
  
```  
// cliext_hash_multiset_hash_delegate.cpp   
// compile with: /clr   
#include <cliext/hash_set>   
  
typedef cliext::hash_multiset<wchar_t> Myhash_multiset;   
int main()   
    {   
    Myhash_multiset c1;   
    Myhash_multiset::hasher^ myhash = c1.hash_delegate();   
  
    System::Console::WriteLine("hash(L'a') = {0}", myhash(L'a'));   
    System::Console::WriteLine("hash(L'b') = {0}", myhash(L'b'));   
    return (0);   
    }  
  
```  
  
```Output  
hash(L'a') = 1616896120  
hash(L'b') = 570892832  
```  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<cliext/hash_set >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>関連項目  
 [hash_multiset (STL/CLR)](../dotnet/hash-multiset-stl-clr.md)   
 [hash_multiset::hasher (STL/CLR)](../dotnet/hash-multiset-hasher-stl-clr.md)