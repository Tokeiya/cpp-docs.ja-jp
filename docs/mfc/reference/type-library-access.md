---
title: "入力ライブラリ アクセス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.mfc.macros
dev_langs: C++
helpviewer_keywords: type libraries [MFC], accessing
ms.assetid: a03fa7f0-86c2-4119-bf81-202916fb74b3
caps.latest.revision: "14"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 8f05738c02fd70fde5fc2d92c5ee1e823747797c
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="type-library-access"></a>タイプ ライブラリ アクセス
タイプ ライブラリは、他の OLE に対応するアプリケーションに対する OLE コントロールのインターフェイスを公開します。 各 OLE コントロールは、1 つまたは複数のインターフェイスを公開する場合、タイプ ライブラリにすることが必要です。  
  
 次のマクロは、独自のタイプ ライブラリへのアクセスを提供する OLE コントロールを許可します。  
  
### <a name="type-library-access"></a>タイプ ライブラリ アクセス  
  
|||  
|-|-|  
|[DECLARE_OLETYPELIB](#declare_oletypelib)|宣言、 `GetTypeLib` (クラス宣言で使用する必要があります) OLE コントロールのメンバー関数。|  
|[IMPLEMENT_OLETYPELIB](#implement_oletypelib)|実装して、 `GetTypeLib` (クラスの実装で使用する必要があります) OLE コントロールのメンバー関数。|  
  
##  <a name="declare_oletypelib"></a>DECLARE_OLETYPELIB  
 宣言、`GetTypeLib`コントロール クラスのメンバー関数。  
  
```   
DECLARE_OLETYPELIB(class_name)   
```  
  
### <a name="parameters"></a>パラメーター  
 *それ以外*  
 タイプ ライブラリに関連するコントロール クラスの名前。  
  
### <a name="remarks"></a>コメント  
 コントロールのクラス ヘッダー ファイルでこのマクロを使用します。  

### <a name="requirements"></a>要件  
 **ヘッダー :** afxdisp.h  

##  <a name="implement_oletypelib"></a>IMPLEMENT_OLETYPELIB  
 コントロールの実装`GetTypeLib`メンバー関数。  
  
```   
IMPLEMENT_OLETYPELIB(class_name, tlid, wVerMajor,  wVerMinor)   
```  
  
### <a name="parameters"></a>パラメーター  
 *それ以外*  
 タイプ ライブラリに関連するコントロール クラスの名前。  
  
 *tlid*  
 タイプ ライブラリの ID 番号。  
  
 `wVerMajor`  
 タイプ ライブラリのメジャー バージョン番号。  
  
 `wVerMinor`  
 タイプ ライブラリのマイナー バージョン番号。  
  
### <a name="remarks"></a>コメント  
 このマクロを使用して任意のコントロール クラスの実装ファイルに表示する必要があります、`DECLARE_OLETYPELIB`マクロです。  

### <a name="requirements"></a>要件  
 **ヘッダー :** afxdisp.h  
   
## <a name="see-also"></a>関連項目  
 [マクロとグローバル](../../mfc/reference/mfc-macros-and-globals.md)
