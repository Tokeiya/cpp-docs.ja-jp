---
title: "マクロの特殊文字 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords: special characters, in NMAKE macros
ms.assetid: c0a06cfc-7103-4ee2-a585-e8f6e85dccd7
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 648122a9c8f3cf97d08128e6e12090ebc12631d9
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="special-characters-in-macros"></a>マクロの特殊文字
コメントを指定する、定義した後のシャープ記号 (#)。 マクロでリテラル シャープ記号を指定するにキャレット (^) ように使用 ^ # です。  
  
 ドル記号 ($) は、マクロの呼び出しを指定します。 $ リテラルを指定するには、$$ を使用します。  
  
 新しい行に、定義を拡張するには、円記号行目の最後 (\\)。 マクロが呼び出されたときに、円記号と改行文字が空白に置き換えられます。 行の末尾にリテラル円記号を指定するキャレット (^) を付けますか、後にコメント指定子 (#)。  
  
 リテラルの改行文字を指定するには、ようにキャレット (^) では、行を終了します。  
  
```  
CMDS = cls^  
dir  
```  
  
## <a name="see-also"></a>関連項目  
 [NMAKE マクロの定義](../build/defining-an-nmake-macro.md)