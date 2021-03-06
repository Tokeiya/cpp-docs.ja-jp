---
title: "Idbschemarowsetimpl::getrowset |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::IDBSchemaRowsetImpl::GetRowset
- ATL.IDBSchemaRowsetImpl.GetRowset
- IDBSchemaRowsetImpl<SessionClass>::GetRowset
- IDBSchemaRowsetImpl.GetRowset
- IDBSchemaRowsetImpl::GetRowset
- ATL::IDBSchemaRowsetImpl<SessionClass>::GetRowset
- GetRowset
dev_langs: C++
helpviewer_keywords: GetRowset method
ms.assetid: 3ae28c22-e186-4a15-8591-b0192e784a6f
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: d2961da1882dcdc607d8dfbefe995e887d74b5ab
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="idbschemarowsetimplgetrowset"></a>IDBSchemaRowsetImpl::GetRowset
スキーマ行セットを返します。  
  
## <a name="syntax"></a>構文  
  
```  
  
      STDMETHOD (GetRowset)(  
   IUnknown *pUnkOuter,  
   REFGUID rguidSchema,  
   ULONG cRestrictions,  
   const VARIANT rgRestrictions[],  
   REFIID riid,  
   ULONG cPropertySets,  
   DBPROPSET rgPropertySets[],  
   IUnknown **ppRowset   
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `pUnkOuter`  
 [入力] 集約時は外部 **IUnknown** 。それ以外の場合は **NULL**。  
  
 `rguidSchema`  
 [入力] 要求するスキーマ行セット GUID ( `DBSCHEMA_TABLES`など) への参照。  
  
 `cRestrictions`  
 [入力] 行セットに適用する制限の数。  
  
 `rgRestrictions`  
 [入力] 制限を表す `cRestrictions`**VARIANT**の配列。  
  
 `riid`  
 [入力] 新しく作成されたスキーマ行セットに対して要求する IID。  
  
 `cPropertySets`  
 [入力] 設定するプロパティ セットの数。  
  
 `rgPropertySets`  
 [入力/出力] 新しく作成されたスキーマ行セットに対して設定する [DBPROPSET](https://msdn.microsoft.com/en-us/library/ms714367.aspx) 構造体の配列。  
  
 `ppRowset`  
 [出力] 新しく作成されたスキーマ行セットに対して要求するインターフェイスへのポインター。  
  
## <a name="remarks"></a>コメント  
 このメソッドを使用するには、ユーザーはセッション クラスにスキーマ マップを持っている必要があります。 `GetRowset` は、 `rguidSchema` パラメーターがいずれかのマップ エントリの GUID と一致する場合、スキーマ マップ情報に基づき、指定された行セット オブジェクトを作成します。 マップ エントリについては、「 [SCHEMA_ENTRY](../../data/oledb/schema-entry.md) 」を参照してください。  
  
 参照してください[idbschemarowset::getrowset](https://msdn.microsoft.com/en-us/library/ms722634.aspx) Windows SDK にします。  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** atldb.h  
  
## <a name="see-also"></a>関連項目  
 [IDBSchemaRowsetImpl クラス](../../data/oledb/idbschemarowsetimpl-class.md)   
 [IDBSchemaRowsetImpl クラス メンバー](http://msdn.microsoft.com/en-us/e74f6f82-541c-42e7-b4c6-e2d4656a0649)   
 [Idbschemarowsetimpl::getschemas](../../data/oledb/idbschemarowsetimpl-getschemas.md)   
 [スキーマ行セット クラスと Typedef クラス](../../data/oledb/schema-rowset-classes-and-typedef-classes.md)