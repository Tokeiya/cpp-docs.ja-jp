---
title: "CommandHandler |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: CommandHandler
dev_langs: C++
helpviewer_keywords: CommandHandler function
ms.assetid: 662bc7bf-4a10-42b3-986d-d8bae4f63551
caps.latest.revision: "13"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: f11e9beee6df4bc4065051242d286fd2ab7dac09
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="commandhandler"></a>CommandHandler
`CommandHandler`3 番目のパラメーターで識別される関数は、`COMMAND_HANDLER`メッセージ マップ マクロです。  
  
## <a name="syntax"></a>構文  
  
```  
 
    LRESULT 
    CommandHandler 
 (
    WORD wNotifyCode,  
    WORD wID,  
    HWND hWndCtl,  
    BOOL& bHandled);
```  
  
#### <a name="parameters"></a>パラメーター  
 `wNotifyCode`  
 通知コード。  
  
 *wID*  
 メニュー項目、コントロール、またはアクセラレータの識別子。  
  
 *hWndCtl*  
 ウィンドウ コントロールへのハンドル。  
  
 `bHandled`  
 メッセージ マップ セット`bHandled`に**TRUE**する前に`CommandHandler`と呼びます。 場合`CommandHandler`、メッセージを完全に処理しませんに設定する必要があります`bHandled`に**FALSE**を示すメッセージがさらに処理を必要があります。  
  
## <a name="return-value"></a>戻り値  
 メッセージの処理の結果。 正常終了した場合は 0 を返します。  
  
## <a name="remarks"></a>コメント  
 メッセージ マップでこのメッセージ ハンドラーを使用しての例は、次を参照してください。 [COMMAND_HANDLER](reference/message-map-macros-atl.md#command_handler)です。  
  
## <a name="see-also"></a>関連項目  
 [ウィンドウの実装](../atl/implementing-a-window.md)   
 [メッセージ マップ](../atl/message-maps-atl.md)   
 [WM_NOTIFY](http://msdn.microsoft.com/library/windows/desktop/bb775583)

