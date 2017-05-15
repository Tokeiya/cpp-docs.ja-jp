---
title: "コンパイラ エラー C2094 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2094
dev_langs:
- C++
helpviewer_keywords:
- C2094
ms.assetid: 9e4f8f88-f189-46e7-91c9-481bacc7af87
caps.latest.revision: 8
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
ms.sourcegitcommit: 6fe065a9cefe7a01942aa3f5411167f8a5f38985
ms.openlocfilehash: a33bc40cd39494a304652ff8b20d40a6f3fdd099
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c2094"></a>コンパイラ エラー C2094
ラベル 'identifier' が定義されていません  
  
使用されるラベル、 [goto](../../cpp/goto-statement-cpp.md)ステートメントが関数に存在しません。  
  
## <a name="example"></a>例  
次の例では C2094 が生成されます。  
  
```cpp  
// C2094.c  
int main() {  
   goto test;  
}   // C2094  
```  
  
 考えられる解決策:  
  
```cpp  
// C2094b.c  
int main() {  
   goto test;  
   test:   
   {  
   }  
}  
```