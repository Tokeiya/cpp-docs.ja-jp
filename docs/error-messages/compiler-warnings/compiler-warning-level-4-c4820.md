---
title: "コンパイラの警告 (レベル 4) C4820 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C4820
dev_langs:
- C++
helpviewer_keywords:
- C4820
ms.assetid: 17aa29f4-c287-49b8-bc43-8ed82ffed5ea
caps.latest.revision: 9
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 3168772cbb7e8127523bc2fc2da5cc9b4f59beb8
ms.openlocfilehash: daf6e41a2e8abf113acdb50282dd7347b112bb76
ms.contentlocale: ja-jp
ms.lasthandoff: 02/24/2017

---
# <a name="compiler-warning-level-4-c4820"></a>コンパイラの警告 (レベル 4) C4820
'バイト' : 'バイト' バイトのパディングを 'コンスラクト' 'member_name' の後に追加しました。  
  
 型と要素の順序は、構造体の末尾にスペースを追加するコンパイラを発生します。 参照してください[align](../../cpp/align-cpp.md)構造体に埋め込みの詳細についてです。  
  
 既定では、この警告はオフに設定されています。 参照してください[コンパイラの警告ことは既定で無効](../../preprocessor/compiler-warnings-that-are-off-by-default.md)の詳細。  
  
 次の例では、C4820 が生成されます。  
  
```  
// C4820.cpp  
// compile with: /W4 /c  
#pragma warning(default : 4820)   
  
// Delete the following 4 lines to resolve.  
__declspec(align(2)) struct MyStruct {  
   char a;  
   int i;   // C4820  
};  
  
// OK  
#pragma pack(1)  
__declspec(align(1)) struct MyStruct2 {  
   char a;  
   int i;  
};  
```
