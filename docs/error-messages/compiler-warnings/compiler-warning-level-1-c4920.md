---
title: "コンパイラの警告 (レベル 1) C4920 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C4920
dev_langs:
- C++
helpviewer_keywords:
- C4920
ms.assetid: 1e501f2e-93c1-4d27-a4fa-54fc86271ae7
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
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: e03b1d14116c6d56774c213738581bfca448cfd1
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-warning-level-1-c4920"></a>コンパイラの警告 (レベル 1) C4920
enum enum member member=value は既に enum enum as member=value に示されています  
  
 #import に渡す .tlb に 2 つ以上の列挙型で定義された同じシンボルが含まれる場合、この警告は、後に続く同じシンボルが無視され、.tlh ファイル内でコメント アウトされることを示します。  
  
 次を含む .tlb を想定します。  
  
```  
library MyLib  
{  
    typedef enum {  
        enumMember = 512  
    } AProblem;  
  
    typedef enum {  
        enumMember = 1024  
    } BProblem;  
};  
```  
  
 次の例では C4920 が生成されます。  
  
```  
// C4920.cpp  
// compile with: /W1  
#import "t4920.tlb"   // C4920  
  
int main() {  
}  
```