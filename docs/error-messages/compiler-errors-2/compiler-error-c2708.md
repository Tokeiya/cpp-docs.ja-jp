---
title: "コンパイラ エラー C2708 |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2708
dev_langs: C++
helpviewer_keywords: C2708
ms.assetid: d52d3088-1141-42f4-829c-74755a7fcc3a
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 8ce9eb29c776c7d98a7fbad4dc95959180045256
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="compiler-error-c2708"></a>コンパイラ エラー C2708
'identifier': 実引数の長さ (バイト単位) は、前の呼び出しまたは参照によって異なります。  
  
 A [_ _stdcall](../../cpp/stdcall.md)関数のプロトタイプで前にする必要があります。 それ以外の場合、コンパイラが関数にプロトタイプとして最初の呼び出しを解釈し、コンパイラと一致しない呼び出しが発生すると、このエラーが発生します。  
  
 修正は、このエラーは、関数プロトタイプを追加します。