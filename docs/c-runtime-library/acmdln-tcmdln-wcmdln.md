---
title: _acmdln, _tcmdln, _wcmdln | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _wcmdln
- _acmdln
apilocation:
- msvcrt.dll
apitype: DLLExport
f1_keywords:
- _acmdln
- acmdln
- _wcmdln
- wcmdln
- _tcmdln
- tcmdln
dev_langs:
- C++
helpviewer_keywords:
- _wcmdln global variable
- wcmdln global variable
- _acmdln global variable
- _tcmdln global variable
- tcmdln global variable
- acmdln global variable
ms.assetid: 4fc0a6a0-3f93-420a-a19f-5276061ba539
caps.latest.revision: 7
author: corob-msft
ms.author: corob
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: f2a5c42313699980828e663727dbc95039c23431
ms.contentlocale: ja-jp
ms.lasthandoff: 05/18/2017

---
# <a name="acmdln-tcmdln-wcmdln"></a>_acmdln, _tcmdln, _wcmdln
内部 CRT グローバル変数。 コマンド ライン。  
  
## <a name="syntax"></a>構文  
  
```  
char * _acmdln;  
wchar_t * _wcmdln;  
  
#ifdef WPRFLAG  
   #define _tcmdln _wcmdln  
#else  
   #define _tcmdln _acmdln  
```  
  
## <a name="remarks"></a>コメント  
 これらの CRT 内部変数には、完全なコマンド ラインが格納されます。 これらは CRT のエクスポートされたシンボルで公開されていますが、コードでの使用が目的ではありません。 `_acmdln` には、データは文字列として格納されます。 `_wcmdln` には、データはワイド文字列として格納されます。 `_tcmdln` は、どちらが適切かに応じて `_acmdln` または`_wcmdln` として定義できます。  
  
## <a name="see-also"></a>関連項目  
 [グローバル変数](../c-runtime-library/global-variables.md)