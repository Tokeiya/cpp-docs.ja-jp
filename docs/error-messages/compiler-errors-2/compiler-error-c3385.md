---
title: "コンパイラ エラー C3385 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3385
dev_langs: C++
helpviewer_keywords: C3385
ms.assetid: 5f1838c1-986e-47db-8dbc-e06976b83cf3
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 9fca91679b6e66ffcaefe5bc169a4889f032cf55
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c3385"></a>コンパイラ エラー C3385
'class::function' : DllImport カスタム属性を含む関数は、クラスのインスタンスを返せません  
  
 `DllImport` 属性を使って指定された .dll ファイルにあるものとして定義されている関数は、クラスのインスタンスを返すことはできません。  
  
 次の例では C3385 が生成されます。  
  
```  
// C3385.cpp  
// compile with: /clr /c  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
struct SomeStruct1 {};  
  
public ref struct Wrap {  
   [ DllImport("somedll.dll", CharSet=CharSet::Unicode) ]  
   static SomeStruct1 f1([In, Out] SomeStruct1 *pS);   // C3385  
};  
```  
