---
title: "Interfacetraits::cancastto メソッド |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: implements/Microsoft::WRL::Details::InterfaceTraits::CanCastTo
dev_langs: C++
helpviewer_keywords: CanCastTo method
ms.assetid: 275847cb-69ea-42bf-910f-05ba6ef8b48d
caps.latest.revision: "5"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 107c89c7643e137b20492f9ae932a736cc0ba603
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="interfacetraitscancastto-method"></a>InterfaceTraits::CanCastTo メソッド
WRL インフラストラクチャをサポートし、コードから直接使用するものではありません。  
  
## <a name="syntax"></a>構文  
  
```  
  
template<typename T>  
static __forceinline bool CanCastTo(  
   _In_ T* ptr,  
   REFIID riid,  
   _Deref_out_ void **ppv  
);  
  
```  
  
#### <a name="parameters"></a>パラメーター  
 `ptr`  
 型へのポインターの名前。  
  
 `riid`  
 インターフェイス ID`Base`です。  
  
 `ppv`  
 この操作が成功すると場合、`ppv`で指定されたインターフェイスを指す`Base`です。 それ以外の場合、`ppv`に設定されている`nullptr`です。  
  
## <a name="return-value"></a>戻り値  
 `true`この操作が成功した場合と`ptr`へのポインターにキャスト`Base`、それ以外の`false`します。  
  
## <a name="remarks"></a>コメント  
 指定したポインターをへのポインターにキャストできるかどうかを示す`Base`です。  
  
 詳細については`Base`、パブリック Typedef セクションを参照して[InterfaceTraits 構造体](../windows/interfacetraits-structure.md)です。  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** implements.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## <a name="see-also"></a>関連項目  
 [InterfaceTraits 構造体](../windows/interfacetraits-structure.md)   
 [Microsoft::WRL::Details 名前空間](../windows/microsoft-wrl-details-namespace.md)