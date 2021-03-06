---
title: "構造化例外処理で C++ を使用して |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-language
ms.tgt_pltfrm: 
ms.topic: language-reference
dev_langs: C++
helpviewer_keywords:
- C++ exception handling, mixed with SEH
- structured exception handling [C++], with C++ exception handling
ms.assetid: ec34b528-8c26-4429-b24a-6a68553aaa91
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 416353ea79bc4ee4e09fe72490a87b70dd6f0029
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="using-structured-exception-handling-with-c"></a>C++ での構造化例外処理の使用
これらの技術情報で説明されている構造化例外処理では、C および C++ ソース ファイルを使用します。 ただし、特に C++ 用にデザインされていないため、推奨されません。 C++ 例外処理を使用して、コードの移植性を高めることができます。 また、C++ 例外処理メカニズムは、任意の型の例外を処理できるという点で、より柔軟です。  
  
 Microsoft C++ は、ANSI C++ 規格に基づいて、C++ の例外処理モデルをサポートするようになりました。 この機構は、スタックのアンワインド中に、自動的にローカル オブジェクトの破棄を処理します。 フォルト トレラントな C++ コードを記述するときに、例外処理を実装する場合は、構造化例外処理ではなく、C++ 例外処理を使用することを強くお勧めします。 (これらの技術情報に説明されているように、C++ コンパイラは構造化例外処理の構造をサポートしますが、標準 C コンパイラは C++ 例外処理の構文をサポートしません)。C++ 例外処理の詳細については、次を参照してください。 [C++ 例外処理](../cpp/cpp-exception-handling.md)と*注解 C++ リファレンス マニュアル*Margaret Ellis と Bjarne Stroustrup でします。  
  
## <a name="see-also"></a>関連項目  
 [構造化例外処理 (C/C++)](../cpp/structured-exception-handling-c-cpp.md)