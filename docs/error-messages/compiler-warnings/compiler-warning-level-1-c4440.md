---
title: "コンパイラの警告 (レベル 1) C4440 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4440
dev_langs: C++
helpviewer_keywords: C4440
ms.assetid: 78b9642a-a93e-401e-9d92-372f6451bc5d
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: b9557791e98a2f3e5ecf58b44170b5c99fb8e30c
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-warning-level-1-c4440"></a>コンパイラの警告 (レベル 1) C4440
呼び出し規約の再 'calling_convention1' から 'calling_convention2' を無視するには  
  
 呼び出し規約の変更は無視されました。  
  
 次の例では、C4440 が生成されます。  
  
```  
// C4440.cpp  
// compile with: /W1 /LD /clr  
typedef void __clrcall F();  
typedef F __cdecl *PFV;   // C4440  
```