---
title: "Windows ランタイムのサポートされていない CRT 関数 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- unsupported CRT functions, Windows Runtime
- Windows Runtime, unsupported CRT functions
ms.assetid: bb8386d6-0ef8-460c-88d8-addff009b6f1
caps.latest.revision: 14
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
ms.sourcegitcommit: 0eb057f9d229c659f339f996d1ff38f65fd2e018
ms.openlocfilehash: be461857f4aa1625094b20a2241ab15853d2aa81
ms.contentlocale: ja-jp
ms.lasthandoff: 06/01/2017

---
# <a name="windows-runtime-unsupported-crt-functions"></a>Windows ランタイムのサポートされていない CRT 関数
多くの C ランタイム (CRT) API は、Windows ランタイムで実行する [!INCLUDE[win8_appname_long](../build/includes/win8_appname_long_md.md)] アプリでは使用できません。 これらのアプリは /ZW コンパイラ フラグを使用してビルドします。 サポートされない CRT 関数の一覧については、「[/ZW でサポートされない CRT 関数](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx)」を参照してください。  
  
 すべての CRT API については、このドキュメントの「[関数リファレンス (アルファベット順)](../c-runtime-library/reference/crt-alphabetical-function-reference.md)」のセクションを参照してください。  
  
## <a name="see-also"></a>関連項目  
 [カテゴリ別ランタイム ルーチン](../c-runtime-library/run-time-routines-by-category.md)   
 [関数リファレンス (アルファベット順)](../c-runtime-library/reference/crt-alphabetical-function-reference.md)