---
title: "コンパイラ エラー C2439 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2439
dev_langs:
- C++
helpviewer_keywords:
- C2439
ms.assetid: 3c5dbe5c-b7d3-4bb0-8619-92f6e280461e
caps.latest.revision: 6
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 6aa5c0dcfd12be6979b0872f001bf0bf26a6e6e7
ms.contentlocale: ja-jp
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2439"></a>コンパイラ エラー C2439
'identifier': メンバーを初期化できませんでした  
  
 クラス、構造体、または共用体のメンバーを初期化することはできません。  
  
### <a name="to-fix-by-checking-the-following-possible-causes"></a>次のような原因をチェックして問題を解決するには  
  
1.  間接基底クラスまたは構造体を初期化しようとしています。  
  
2.  クラスまたは構造体の継承されたメンバーを初期化しようとしています。 継承されたメンバーは、クラスまたは構造体のコンス トラクターによって初期化する必要があります。
