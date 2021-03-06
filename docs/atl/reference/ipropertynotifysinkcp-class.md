---
title: "IPropertyNotifySinkCP クラス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- IPropertyNotifySinkCP
- atlctl/ATL::IPropertyNotifySinkCP
dev_langs: C++
helpviewer_keywords:
- connection points [C++], managing
- sinks, notifying of changes
- IPropertyNotifySinkCP class
ms.assetid: 1b41445e-bc88-4fa6-bb62-d68aacec2bd5
caps.latest.revision: "21"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 91e2bcff0b168e9238351cff623f888221b583b2
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="ipropertynotifysinkcp-class"></a>IPropertyNotifySinkCP クラス
このクラスは、公開[IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638)接続可能なオブジェクトに対する発信インターフェイスとしてインターフェイスです。  
  
> [!IMPORTANT]
>  このクラスとそのメンバーは、Windows ランタイムで実行するアプリケーションでは使用できません。  
  
## <a name="syntax"></a>構文  
  
```
template<class T, class CDV = CComDynamicUnkArray>  
class IPropertyNotifySinkCP 
   : public IConnectionPointImpl<T, &IID_IPropertyNotifySink, CDV>
```    
  
#### <a name="parameters"></a>パラメーター  
 `T`  
 派生したクラス、`IPropertyNotifySinkCP`です。  
  
 `CDV`  
 接続ポイントとそのシンク間の接続を管理するクラス。 既定値は[CComDynamicUnkArray](../../atl/reference/ccomdynamicunkarray-class.md)、無制限の接続を許可します。 使用することも[CComUnkArray](../../atl/reference/ccomunkarray-class.md)、固定接続数を指定します。  
  
## <a name="remarks"></a>コメント  
 `IPropertyNotifySinkCP`その基本クラスを使って、すべてのメソッドを継承[IConnectionPointImpl](../../atl/reference/iconnectionpointimpl-class.md)です。  
  
 [IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638)インターフェイスにより、シンク オブジェクト プロパティの変更に関する通知を受信します。 クラス`IPropertyNotifySinkCP`接続可能なオブジェクトに対する発信インターフェイスとしてこのインターフェイスを公開します。 クライアントを実装する必要があります、`IPropertyNotifySink`シンクのメソッドです。  
  
 クラスを派生`IPropertyNotifySinkCP`を表す接続ポイントを作成する場合、`IPropertyNotifySink`インターフェイスです。  
  
 ATL の接続ポイントの使い方の詳細については、記事を参照してください。[コネクション ポイント](../../atl/atl-connection-points.md)です。  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** atlctl.h  
  
## <a name="see-also"></a>関連項目  
 [IConnectionPointImpl クラス](../../atl/reference/iconnectionpointimpl-class.md)   
 [入力したコネクション クラス](../../atl/reference/iconnectionpointcontainerimpl-class.md)   
 [クラスの概要](../../atl/atl-class-overview.md)
