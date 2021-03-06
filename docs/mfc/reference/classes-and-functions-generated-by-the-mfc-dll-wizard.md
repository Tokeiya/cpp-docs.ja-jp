---
title: "クラスと MFC DLL ウィザードによって生成される関数 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- functions [MFC]
- functions [MFC], DLLs
- MFC DLL Wizard
- DLLs [MFC], wizard classes and functions
- classes [MFC], generated by MFC DLL wizard
- code [MFC], generated by MFC DLL wizard
ms.assetid: e69e62fe-4953-42bf-a2fc-50bbf9bdaeaf
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 52465b01b8644b2f4ea1f4a22412af0159e4f598
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="classes-and-functions-generated-by-the-mfc-dll-wizard"></a>MFC DLL ウィザードによって生成されるクラスと関数
MFC DLL ウィザードによって生成されるコードは、DLL を作成し、選択したオプションの種類によって異なります。 MFC DLL ウィザードでは、標準の MFC Dll の両方の形式を同じコードを生成します。  
  
|DLL の種類|オプション|クラス|関数|  
|-----------------|------------|-------------|---------------|  
|[拡張機能](../../build/extension-dlls-overview.md)|なし|なし|`DllMain`|  
|[通常](../../build/regular-dlls-dynamically-linked-to-mfc.md)|なし|を派生したアプリケーション クラス`CWinApp`|なし|  
|[通常](../../build/regular-dlls-dynamically-linked-to-mfc.md)|オートメーション|を派生したアプリケーション クラス`CWinApp`|**DllGetClassObjectDllCanUnloadNowDllRegisterServer**|  
|[拡張機能](../../build/extension-dlls-overview.md)|ウィンドウのソケット|なし|`DllMain`|  
|[通常](../../build/regular-dlls-dynamically-linked-to-mfc.md)|ウィンドウのソケット|を派生したアプリケーション クラス`CWinApp`|`InitInstance`呼び出しが含まれています`AfxSocketInit`|  
  
## <a name="see-also"></a>関連項目  
 [MFC DLL ウィザード](../../mfc/reference/mfc-dll-wizard.md)

