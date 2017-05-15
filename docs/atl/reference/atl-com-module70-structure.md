---
title: "_ATL_COM_MODULE70 構造 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::_ATL_COM_MODULE70
- ATL._ATL_COM_MODULE70
- _ATL_COM_MODULE70
dev_langs:
- C++
helpviewer_keywords:
- _ATL_COM_MODULE70 structure
- ATL_COM_MODULE70 structure
ms.assetid: 5b0b2fd0-bdeb-4c7e-8870-78fa69ace6e6
caps.latest.revision: 15
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
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
translationtype: Machine Translation
ms.sourcegitcommit: 4e393abb2a904a0f5e101efe3d78d0645664397b
ms.openlocfilehash: 503c2a29cf0e70020b012911c51b056f00562374
ms.lasthandoff: 02/24/2017

---
# <a name="atlcommodule70-structure"></a>_ATL_COM_MODULE70 構造体
ATL で COM に関連するコードで使用されます。  
  
## <a name="syntax"></a>構文  
  
```
struct _ATL_COM_MODULE70 {
    UINT cbSize;
    HINSTANCE m_hInstTypeLib;
    _ATL_OBJMAP_ENTRY** m_ppAutoObjMapFirst;
    _ATL_OBJMAP_ENTRY** m_ppAutoObjMapLast;
    CRITICAL_SECTION m_csObjMap;
};
```  
  
## <a name="members"></a>メンバー  
 `cbSize`  
 バージョン管理に使用される、構造体のサイズ。  
  
 `m_hInstTypeLib`  
 このモジュールのタイプ ライブラリへのハンドルのインスタンス。  
  
 **m_ppAutoObjMapFirst**  
 このモジュールのオブジェクトのマップ エントリの先頭を示す配列の要素のアドレスです。  
  
 **m_ppAutoObjMapLast**  
 このモジュールのオブジェクトのマップ エントリの終わりを示す配列の要素のアドレスです。  
  
 `m_csObjMap`  
 オブジェクト マップ エントリへのアクセスをシリアル化するクリティカル セクション。 ATL で内部的に使用  
  
## <a name="remarks"></a>コメント  
 [_ATL_COM_MODULE](atl-typedefs.md#_atl_com_module)の typedef と定義`_ATL_COM_MODULE70`します。  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** atlbase.h  
  
## <a name="see-also"></a>関連項目  
 [構造体](../../atl/reference/atl-structures.md)





