---
title: "ANSI C 準拠 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- Ansi
dev_langs:
- C++
helpviewer_keywords:
- underscores, leading
- compatibility [C++], ANSI C
- compliance with ANSI C
- conventions [C++], Microsoft extensions
- underscores
- naming conventions [C++], Microsoft library
- ANSI [C++], C standard
- Microsoft extensions naming conventions
ms.assetid: 6be271bf-eecf-491a-a928-0ee2dd60e3b9
caps.latest.revision: 6
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d6eb43b2e77b11f4c85f6cf7e563fe743d2a7093
ms.openlocfilehash: 7e6c5d4045f0b71890a34d845b898844ca550ca8
ms.contentlocale: ja-jp
ms.lasthandoff: 05/18/2017

---
# <a name="ansi-c-compliance"></a>ANSI C 準拠
ランタイム システムのすべての Microsoft 固有の識別子 (関数、マクロ、定数、変数、型の定義など) の名前付け規則は、ANSI に準拠しています。 このドキュメントでは、ANSI/ISO C 標準に従うランタイム関数は、いずれも ANSI 互換であることが記載されています。 ANSI 準拠アプリケーションでは、これらの ANSI 互換の関数だけを使用してください。  
  
 Microsoft 固有の関数とグローバル変数の名前は、1 つのアンダースコアで始まります。 これらの名前は、ローカルでのみ、コードのスコープ内で上書きできます。 たとえば、Microsoft ランタイム ヘッダー ファイルをインクルードするとき、`_open` という名前の Microsoft 固有の関数を、同じ名前のローカル変数を宣言することで上書きできます。 ただし、独自のグローバル関数またはグローバル変数としてこの名前を使用することはできません。  
  
 Microsoft 固有のマクロとマニフェスト定数の名前は、2 つのアンダー スコア、または先頭の 1 つのアンダースコアとその直後の大文字で始まります。 これらの識別子のスコープは絶対です。 たとえば、この理由から Microsoft 固有の識別子 **_UPPER** を使用することはできません。  
  
## <a name="see-also"></a>関連項目  
 [互換性](../c-runtime-library/compatibility.md)