---
title: "コンパイラ エラー C2557 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2557
dev_langs:
- C++
helpviewer_keywords:
- C2557
ms.assetid: 48a33d82-aa16-4658-b346-2311fcb39864
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
ms.openlocfilehash: 188adf139e1fd4857eaa0a50e49ca9971cb0f8aa
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2557"></a>コンパイラ エラー C2557
'identifier': プライベート メンバー、プロテクト メンバーの初期化にはコンストラクターが必要です  
  
 プライベート メンバーまたはプロテクト メンバーに値を割り当てることができるのは、メンバーとフレンドのみです。 非パブリック メンバーは、クラス コンストラクターで初期化する必要があります。