---
title: "致命的なエラー C1103 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1103
dev_langs:
- C++
helpviewer_keywords:
- C1103
ms.assetid: 9d276939-9c47-4235-9d20-76b8434f9731
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: e750c21ab6f9d3882413a83731c0fa2787f8fe47
ms.contentlocale: ja-jp
ms.lasthandoff: 04/12/2017

---
# <a name="fatal-error-c1103"></a>致命的なエラー C1103
progid をインポート中の致命的なエラー: 'message'  
  
 コンパイラがタイプ ライブラリのインポートで問題を検出しました。  たとえば、progid を持つタイプ ライブラリを指定し、さらに `no_registry`を指定することはできません。  
  
 詳細については、次を参照してください。 [#import ディレクティブ](../../preprocessor/hash-import-directive-cpp.md)です。  
  
 次の例では C1103 エラーが生成されます。  
  
```  
// C1103.cpp  
#import "progid:a.b.id.1.5" no_registry auto_search   // C1103  
```