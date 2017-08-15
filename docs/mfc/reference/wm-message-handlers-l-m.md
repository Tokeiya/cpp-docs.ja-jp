---
title: "Wm _ で始まるメッセージのハンドラー: L-M |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ON_WM_MENUSELECT
- ON_WM_MBUTTONDBLCLK
- ON_WM_MOUSEACTIVATE
- ON_WM_MOUSEMOVE
- ON_WM_MOVING
- ON_WM_LBUTTONUP
- ON_WM_LBUTTONDBLCLK
- ON_WM_MEASUREITEM
- ON_WM_MDIACTIVATE
- ON_WM_MOVE
- ON_WM_LBUTTONDOWN
- ON_WM_MBUTTONDOWN
- ON_WM_MENUCHAR
- ON_WM_MBUTTONUP
dev_langs:
- C++
helpviewer_keywords:
- ON_WM_MENUSELECT
- ON_WM_MBUTTONDBLCLK
- ON_WM_MOVE
- ON_WM_MOUSEACTIVATE
- ON_WM_MBUTTONUP
- ON_WM_MOUSEMOVE
- ON_WM_MENUCHAR
- ON_WM_MBUTTONDOWN
- ON_WM_MEASUREITEM
- ON_WM_MOVING
- ON_WM_LBUTTONDOWN
- ON_WM_MDIACTIVATE
- ON_WM_LBUTTONDBLCLK
- ON_WM_LBUTTONUP
- WM_ messages
ms.assetid: 96ecaaf1-6d13-4e12-a454-535635967489
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 040985df34f2613b4e4fae29498721aef15d50cb
ms.openlocfilehash: 645e8ef051624977571830f2f1b40e54c55603f0
ms.contentlocale: ja-jp
ms.lasthandoff: 02/24/2017

---
# <a name="wm-message-handlers-l---m"></a>WM_ で始まるメッセージのハンドラー : L - M
左側の次のマップ エントリは、右側の関数プロトタイプに対応しています。  
  
|マップ エントリ|関数プロトタイプ|  
|---------------|------------------------|  
|ON_WM_LBUTTONDBLCLK()|afx_msg void[離し](../../mfc/reference/cwnd-class.md#onlbuttondblclk)(UINT、CPoint) です。|  
|ON_WM_LBUTTONDOWN()|afx_msg void [OnLButtonDown](../../mfc/reference/cwnd-class.md#onlbuttondown)(UINT、CPoint) です。|  
|ON_WM_LBUTTONUP()|afx_msg void [OnLButtonUp](../../mfc/reference/cwnd-class.md#onlbuttonup)(UINT、CPoint) です。|  
|ON_WM_MBUTTONDBLCLK()|afx_msg void[離し](../../mfc/reference/cwnd-class.md#onmbuttondblclk)(UINT、CPoint) です。|  
|ON_WM_MBUTTONDOWN()|afx_msg void [OnMButtonDown](../../mfc/reference/cwnd-class.md#onmbuttondown)(UINT、CPoint) です。|  
|ON_WM_MBUTTONUP()|afx_msg void [OnMButtonUp](../../mfc/reference/cwnd-class.md#onmbuttonup)(UINT、CPoint) です。|  
|ON_WM_MDIACTIVATE()|afx_msg void[なる](../../mfc/reference/cwnd-class.md#onmdiactivate)(BOOL、CWnd * CWnd\*) です。|  
|ON_WM_MEASUREITEM()|afx_msg void [OnMeasureItem](../../mfc/reference/cwnd-class.md#onmeasureitem)(LPMEASUREITEMSTRUCT) です。|  
|ON_WM_MENUCHAR()|時間の長い afx_msg [OnMenuChar](../../mfc/reference/cwnd-class.md#onmenuchar)(UINT、UINT、CMenu *)。|  
|ON_WM_MENUDRAG()|afx_msg UINT [OnMenuDrag](../../mfc/reference/cwnd-class.md#onmenudrag)(UINT、CMenu *)。|  
|ON_WM_MENUGETOBJECT()|afx_msg UINT [OnMenuGetObject](../../mfc/reference/cwnd-class.md#onmenugetobject)(MENUGETOBJECTINFO *)。|  
|ON_WM_MENURBUTTONUP()|afx_msg void [OnMenuRButtonUp](../../mfc/reference/cwnd-class.md#onmenurbuttonup)(UINT、CMenu *)。|  
|ON_WM_MENUSELECT()|afx_msg void [OnMenuSelect](../../mfc/reference/cwnd-class.md#onmenuselect)(UINT、UINT、HMENU)|  
|ON_WM_MOUSEACTIVATE()|afx_msg int [OnMouseActivate](../../mfc/reference/cwnd-class.md#onmouseactivate)(CWnd *、UINT、UINT) です。|  
|ON_WM_MOUSEHOVER()|afx_msg void [OnMouseHover](../../mfc/reference/cwnd-class.md#onmousehover)(UINT、CPoint) です。|  
|ON_WM_MOUSEHWHEEL()|afx_msg void [OnMouseHWheel](../../mfc/reference/cwnd-class.md#onmousehwheel)(UINT、short、CPoint) です。|  
|ON_WM_MOUSELEAVE()|afx_msg void [OnMouseLeave](../../mfc/reference/cwnd-class.md#onmouseleave)();|  
|ON_WM_MOUSEMOVE()|afx_msg void [OnMouseMove](../../mfc/reference/cwnd-class.md#onmousemove)(UINT、CPoint) です。|  
|ON_WM_MOUSEWHEEL()|afx_msg BOOL [OnMouseWheel](../../mfc/reference/cwnd-class.md#onmousewheel)(UINT、short、CPoint) です。|  
|ON_WM_MOVE()|afx_msg void [OnMove](../../mfc/reference/cwnd-class.md#onmove)(int、int) です。|  
|ON_WM_MOVING()|afx_msg void [OnMoving](../../mfc/reference/cwnd-class.md#onmoving)(UINT、LPRECT) です。|  
  
## <a name="see-also"></a>関連項目  
 [メッセージ マップ](../../mfc/reference/message-maps-mfc.md)   
 [Wm _ で始まるメッセージのハンドラー](../../mfc/reference/handlers-for-wm-messages.md)

