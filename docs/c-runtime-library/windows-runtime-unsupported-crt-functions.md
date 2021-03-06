---
title: "Windows ランタイムのサポートされていない CRT 関数 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- unsupported CRT functions, Windows Runtime
- Windows Runtime, unsupported CRT functions
ms.assetid: bb8386d6-0ef8-460c-88d8-addff009b6f1
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: f9fb74dbc28235f211f24d64ef125f2cccdafc7d
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="windows-runtime-unsupported-crt-functions"></a>Windows ランタイムのサポートされていない CRT 関数
多くの C ランタイム (CRT) API は、Windows ランタイムで実行する [!INCLUDE[win8_appname_long](../build/includes/win8_appname_long_md.md)] アプリでは使用できません。 これらのアプリは /ZW コンパイラ フラグを使用してビルドします。 サポートされない CRT 関数の一覧については、「[/ZW でサポートされない CRT 関数](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx)」を参照してください。  
  
 すべての CRT API については、このドキュメントの「[関数リファレンス (アルファベット順)](../c-runtime-library/reference/crt-alphabetical-function-reference.md)」のセクションを参照してください。  
  
## <a name="see-also"></a>関連項目  
 [カテゴリ別ランタイム ルーチン](../c-runtime-library/run-time-routines-by-category.md)   
 [関数リファレンス (アルファベット順)](../c-runtime-library/reference/crt-alphabetical-function-reference.md)