---
title: "max_unbounded クラス | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- allocators/stdext::max_unbounded
- stdext::max_unbounded
- max_unbounded
- allocators/stdext::max_unbounded::allocated
- allocators/stdext::max_unbounded::deallocated
- allocators/stdext::max_unbounded::full
- allocators/stdext::max_unbounded::released
- allocators/stdext::max_unbounded::saved
dev_langs:
- C++
helpviewer_keywords:
- max_unbounded class
ms.assetid: e34627a9-c231-4031-a483-cbb0514fff46
caps.latest.revision: 18
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.mt:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
ms.translationtype: Machine Translation
ms.sourcegitcommit: 66798adc96121837b4ac2dd238b9887d3c5b7eef
ms.openlocfilehash: c12c03d734b411767e7aeef1c2c541103e5ff286
ms.contentlocale: ja-jp
ms.lasthandoff: 04/29/2017

---
# <a name="maxunbounded-class"></a>max_unbounded クラス
[freelist](../standard-library/freelist-class.md) オブジェクトの最長値を制限しない[最大クラス](../standard-library/allocators-header.md) オブジェクトを記述します。  
  
## <a name="syntax"></a>構文  
  
```
class max_unbounded
```  
  
### <a name="member-functions"></a>メンバー関数  
  
|||  
|-|-|  
|[allocated](#allocated)|割り当てられたメモリ ブロックの数を増やします。|  
|[deallocated](#deallocated)|割り当てられたメモリ ブロックの数を減らします。|  
|[full](#full)|フリー リストにメモリ ブロックを追加する必要があるかどうかを示す値を返します。|  
|[released](#released)|フリー リスト上のメモリ ブロックの数を減らします。|  
|[saved](#saved)|フリー リスト上のメモリ ブロックの数を減らします。|  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** \<allocators>  
  
 **名前空間:** stdext  
  
##  <a name="allocated"></a>  max_unbounded::allocated  
 割り当てられたメモリ ブロックの数を増やします。  
  
```
void allocated(std::size_t _Nx = 1);
```  
  
### <a name="parameters"></a>パラメーター  
  
|パラメーター|説明|  
|---------------|-----------------|  
|`_Nx`|増分値。|  
  
### <a name="remarks"></a>コメント  
 このメンバー関数は何も処理を行いません。 `cache_freelist::allocate` による演算子 `new` への呼び出しが成功するたび、その後に呼び出されます。 引数 `_Nx` は、演算子 `new` によって割り当てられたチャンク内のメモリ ブロックの数です。  
  
##  <a name="deallocated"></a>  max_unbounded::deallocated  
 割り当てられたメモリ ブロックの数を減らします。  
  
```
void deallocated(std::size_t _Nx = 1);
```  
  
### <a name="parameters"></a>パラメーター  
  
|パラメーター|説明|  
|---------------|-----------------|  
|`_Nx`|増分値。|  
  
### <a name="remarks"></a>コメント  
 このメンバー関数は何も処理を行いません。 このメンバー関数は、`cache_freelist::deallocate` による演算子 `delete` への呼び出しがあるたび、その後に呼び出されます。 引数 `_Nx` は、演算子 `delete` によって割り当て解除されたチャンク内のメモリ ブロックの数です。  
  
##  <a name="full"></a>  max_unbounded::full  
 フリー リストにメモリ ブロックを追加する必要があるかどうかを示す値を返します。  
  
```
bool full();
```  
  
### <a name="return-value"></a>戻り値  
 このメンバー関数は常に `false` を返します。  
  
### <a name="remarks"></a>コメント  
 このメンバー関数は `cache_freelist::deallocate` によって呼び出されます。 呼び出しが `true` を返すと、`deallocate` はメモリ ブロックをフリー リストに置きます。false を返す場合は、`deallocate` は演算子 `delete` を呼び出してブロックの割り当てを解除します。  
  
##  <a name="released"></a>  max_unbounded::released  
 フリー リスト上のメモリ ブロックの数を減らします。  
  
```
void released();
```  
  
### <a name="remarks"></a>コメント  
 このメンバー関数は何も処理を行いません。 現在の最大クラスの `released` メンバー関数は、`cache_freelist::allocate` によって、フリー リストからメモリ ブロックが削除されるたびに、呼び出されます。  
  
##  <a name="saved"></a>  max_unbounded::saved  
 フリー リスト上のメモリ ブロックの数を減らします。  
  
```
void saved();
```  
  
### <a name="remarks"></a>コメント  
 このメンバー関数は何も処理を行いません。 `cache_freelist::deallocate` によって、フリー リストにメモリ ブロックが置かれるたびに、呼び出されます。  
  
## <a name="see-also"></a>関連項目  
 [\<allocators>](../standard-library/allocators-header.md)



