---
title: "コンパイラ エラー C3394 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3394
dev_langs:
- C++
helpviewer_keywords:
- C3394
ms.assetid: 4e025d79-27ba-43c8-b0d9-839ecef98126
caps.latest.revision: 5
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
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: 9a0184512f1817e3f2de7119f483a2f5b5801344
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-error-c3394"></a>コンパイラ エラー C3394
制約句の構文エラー: 'identifier' が見つかりましたが、型を指定しなければなりません  
  
 制約の形式が間違っています。  詳細については、次を参照してください。[ジェネリック型パラメーターの制約 (C + +/CLI)](../../windows/constraints-on-generic-type-parameters-cpp-cli.md)します。  
  
## <a name="example"></a>例  
 次の例では C3394 が生成されます。  
  
```  
// C3394.cpp  
// compile with: /clr /c  
ref class MyClass {};  
ref class R {  
   generic<typename T>  
   where T : static   // C3394  
   // try the following line instead  
   // where T : MyClass  
   void f() {}  
};  
```