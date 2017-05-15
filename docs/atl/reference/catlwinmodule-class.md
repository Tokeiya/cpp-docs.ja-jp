---
title: "CAtlWinModule クラス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CAtlWinModule
- ATLBASE/ATL::CAtlWinModule
- ATLBASE/ATL::CAtlWinModule::CAtlWinModule
- ATLBASE/ATL::CAtlWinModule::AddCreateWndData
- ATLBASE/ATL::CAtlWinModule::ExtractCreateWndData
dev_langs:
- C++
helpviewer_keywords:
- CAtlWinModule class
ms.assetid: 7ec844af-0f68-4a34-b0c8-9de50a025df0
caps.latest.revision: 20
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
ms.sourcegitcommit: d2d39abf526a58b8442107b5ee816f316ae841f5
ms.openlocfilehash: f2d5e28f39159b097c4e00e11518295b2872a84b
ms.lasthandoff: 03/31/2017

---
# <a name="catlwinmodule-class"></a>CAtlWinModule クラス
このクラスは、ATL の windowing コンポーネントのサポートを提供します。  
  
> [!IMPORTANT]
>  このクラスとそのメンバーは、Windows ランタイムで実行するアプリケーションでは使用できません。  
  
## <a name="syntax"></a>構文  
  
```
class CAtlWinModule : public _ATL_WIN_MODULE
```  
  
## <a name="members"></a>メンバー  
  
### <a name="public-constructors"></a>パブリック コンストラクター  
  
|名前|説明|  
|----------|-----------------|  
|[CAtlWinModule::CAtlWinModule](#catlwinmodule)|コンストラクターです。|  
|[CAtlWinModule:: ~ CAtlWinModule](#dtor)|デストラクターです。|  
  
### <a name="public-methods"></a>パブリック メソッド  
  
|名前|説明|  
|----------|-----------------|  
|[CAtlWinModule::AddCreateWndData](#addcreatewnddata)|データ オブジェクトを追加します。|  
|[CAtlWinModule::ExtractCreateWndData](#extractcreatewnddata)|ウィンドウのモジュールのデータ オブジェクトへのポインターを返します。|  
  
## <a name="remarks"></a>コメント  
 このクラスは、windowing 機能を必要とするすべての ATL クラスのサポートを提供します。  
  
## <a name="inheritance-hierarchy"></a>継承階層  
 [_ATL_WIN_MODULE](atl-typedefs.md#_atl_win_module)  
  
 `CAtlWinModule`  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** atlbase.h  
  
##  <a name="addcreatewnddata"></a>CAtlWinModule::AddCreateWndData  
 このメソッドを初期化し、追加、`_AtlCreateWndData`構造体。  
  
```
void AddCreateWndData(_AtlCreateWndData* pData, void* pObject);
```  
  
### <a name="parameters"></a>パラメーター  
 `pData`  
 ポインター、`_AtlCreateWndData`構造体を初期化し、現在のモジュールに追加します。  
  
 `pObject`  
 オブジェクトへのポインター**この**ポインター。  
  
### <a name="remarks"></a>コメント  
 このメソッドを呼び出す[AtlWinModuleAddCreateWndData](winmodule-global-functions.md#atlwinmoduleaddcreatewnddata)どの初期化、 [_AtlCreateWndData](../../atl/reference/atlcreatewnddata-structure.md)構造体。 この構造体を格納する、**この**ポインター、ウィンドウ プロシージャ内のクラスのインスタンスを取得するために使用します。  
  
##  <a name="catlwinmodule"></a>CAtlWinModule::CAtlWinModule  
 コンストラクターです。  
  
```
CAtlWinModule();
```  
  
### <a name="remarks"></a>コメント  
 初期化に失敗した場合、 **EXCEPTION_NONCONTINUABLE**例外が発生します。  
  
##  <a name="dtor"></a>CAtlWinModule:: ~ CAtlWinModule  
 デストラクターです。  
  
```
~CAtlWinModule();
```  
  
### <a name="remarks"></a>コメント  
 割り当てられているすべてのリソースを解放します。  
  
##  <a name="extractcreatewnddata"></a>CAtlWinModule::ExtractCreateWndData  
 このメソッドへのポインターを返します、`_AtlCreateWndData`構造体。  
  
```
void* ExtractCreateWndData();
```  
  
### <a name="return-value"></a>戻り値  
 ポインターを返します、`_AtlCreateWndData`構造に追加した[CAtlWinModule::AddCreateWndData](#addcreatewnddata)、またはオブジェクトがない場合は NULL です。  
  
## <a name="see-also"></a>関連項目  
 [_ATL_WIN_MODULE](atl-typedefs.md#_atl_win_module)   
 [クラスの概要](../../atl/atl-class-overview.md)   
 [モジュール クラス](../../atl/atl-module-classes.md)
