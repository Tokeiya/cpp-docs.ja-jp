---
title: "型キャスト変換 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "変換 [C++], 型キャスト"
  - "データ型変換 [C++], 型キャストの変換"
  - "明示的な型変換"
  - "型キャスト"
  - "型キャスト [C++], 型キャストの変換の概要"
  - "型キャストの変換 [C++]"
ms.assetid: 57ab5902-f12f-4326-a2f6-6282f1d4025a
caps.latest.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 8
---
# 型キャスト変換
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

型キャストを使用して、明示的に型を変換できます。  
  
 **構文**  
  
 *cast\-expression*:  
 *unary expression*  
  
 **\(**  *type\-name*  **\)**  *cast\-expression*  
  
 *type\-name*:  
 *specifier\-qualifier\-list abstract\-declarator*  opt  
  
 *type\-name* は型であり、*cast\-expression* は、その型に変換される値です。  型キャストがある式は左辺値ではありません。  *cast\-expression* は、*type\-name* 型の変数に代入されたかのように変換されます。  代入の変換規則 \(「[Assignment Conversions \(代入変換\)](../c-language/assignment-conversions.md)」を参照\) は、型キャストにも適用されます。  特定の型にキャストできる型を次の表に示します。  
  
### 有効な型キャスト  
  
|変換先の型|可能性のある変換元|  
|-----------|---------------|  
|整数型|任意の整数型または浮動小数点型、またはオブジェクトへのポインター|  
|浮動小数点数|任意の数値型|  
|オブジェクトへのポインター、または \(**void \***\)|任意の整数型、\(**void \***\)、オブジェクトへのポインター、または関数ポインター|  
|関数ポインター|任意の整数型、オブジェクトへのポインター、または関数ポインター|  
|構造体、共用体、または配列|なし|  
|void 型|任意の型|  
  
 `void` 型には、任意の識別子からキャストできます。  ただし、型キャスト式で指定された型が `void` でない場合、その型にキャストされている識別子を `void` 式にすることはできません。  任意の式を `void` にキャストできますが、`void` 型の式を他の型にキャストすることはできません。  たとえば、戻り値の型が `void` の関数では、戻り値を別の型にキャストすることはできません。  
  
 **void \*** 式は、`void` 型ではなく、`void` への型ポインターを持つことに注意してください。  オブジェクトが `void` 型にキャストされる場合、結果の式はどの項目にも代入できません。  同様に、型キャスト オブジェクトは許容される左辺値ではないので、型キャスト オブジェクトへの代入はできません。  
  
 **Microsoft 固有の仕様 →**  
  
 識別子のサイズが変更されない限り、型キャストを左辺値の式にできます。  左辺値式の詳細については、「[左辺値と右辺値の式](../Topic/L-Value%20and%20R-Value%20Expressions.md)」を参照してください。  
  
 **END Microsoft 固有の仕様**  
  
 キャストで式を型 `void` に変換できますが、その結果の式を使用できるのは、値が不要な場合のみです。  **void \*** に変換され、元の型に戻されたオブジェクト ポインターは、元の値に戻ります。  
  
## 参照  
 [型変換](../c-language/type-conversions-c.md)