---
title: "リリース ビルド |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- debugging [C++], release builds
- release builds
- debug builds, converting to release build
ms.assetid: fa9a78fa-f4b5-4722-baf4-aec655c4ff0f
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: b6ba275b3a287130df111ba89ec2f4dd91170d17
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="release-builds"></a>リリース ビルド
リリース ビルドでは、最適化を使用します。 最適化を使用して、リリース ビルドを作成するときに、コンパイラには、シンボリック デバッグ情報は生成されません。 トレースと ASSERT コードが生成されないことのファクトと共に、シンボリック デバッグ情報がない場合を呼び出すと、実行可能ファイルのサイズが少なくなり、高速化できるためことを意味します。  
  
 このセクションでは、デバッグ ビルドからリリース ビルドに変更する理由とタイミングに関する情報を示します。 また、いくつかのデバッグ、リリース ビルドを変更するときに発生する問題について説明します。  
  
-   [リリース ビルドを作成します。](../../build/reference/how-to-create-a-release-build.md)  
  
-   [リリース ビルド作成時によくある問題](../../build/reference/common-problems-when-creating-a-release-build.md)  
  
-   [リリース ビルドの問題の解決](../../build/reference/fixing-release-build-problems.md)  
  
    -   [ASSERT ステートメントを確認します。](../../build/reference/using-verify-instead-of-assert.md)  
  
    -   [メモリ上書きのチェックにデバッグ ビルドを使用します。](../../build/reference/using-the-debug-build-to-check-for-memory-overwrite.md)  
  
    -   [リリース ビルドのデバッグ](../../build/reference/how-to-debug-a-release-build.md)  
  
    -   [メモリ上書きのチェック](../../build/reference/checking-for-memory-overwrites.md)  
  
## <a name="see-also"></a>関連項目  
 [Visual Studio での C++ プロジェクトのビルド](../../ide/building-cpp-projects-in-visual-studio.md)   
 [C/C++ ビルドのリファレンス](../../build/reference/c-cpp-building-reference.md)