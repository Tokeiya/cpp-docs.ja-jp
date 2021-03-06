---
title: "-WX (リンカー警告として扱うエラー) |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: /WX
dev_langs: C++
helpviewer_keywords:
- /WX linker option
- -WX linker option
- WX linker option
ms.assetid: e4ba97c7-93f7-43ae-a4bb-d866790926c9
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: a4624436ac3109286749d654fb90d4318a837bc0
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="wx-treat-linker-warnings-as-errors"></a>/WX (リンカー警告をエラーとして扱う)
```  
/WX[:NO]  
```  
  
## <a name="remarks"></a>コメント  
 /WX には、リンカーは警告を生成する場合に生成する出力ファイルは行われません。  
  
 似ています**/WX**コンパイラ (を参照してください[/w、/W0、/W1、/W2、/W3、/W4、/w1、/w2、/w3、/w4、/Wall、/wd、//wo、/Wv、/WX (警告レベル)](../../build/reference/compiler-option-warning-level.md)詳細については)。 ただしを指定する**/WX**のコンパイルとは限りませんを**/WX**リンク フェーズが有効にもなります。 明示的に指定する必要があります**/WX**各ツールのです。  
  
 既定では、 **/WX**は無効です。 リンカー警告をエラーとして扱うするには指定**/WX**です。 **/WX:NO**を指定しないと同じ**/WX**です。  
  
### <a name="to-set-this-linker-option-in-the-visual-studio-development-environment"></a>Visual Studio 開発環境でこのリンカー オプションを設定するには  
  
1.  プロジェクトの **[プロパティ ページ]** ダイアログ ボックスを開きます。 詳細については、「 [Visual C プロジェクト プロパティの設定](../../ide/working-with-project-properties.md)です。  
  
2.  クリックして、**リンカー**フォルダーです。  
  
3.  **[コマンド ライン]** プロパティ ページをクリックします。  
  
4.  オプションを入力、**追加オプション**ボックス。  
  
### <a name="to-set-this-linker-option-programmatically"></a>このリンカーをコードから設定するには  
  
1.  「<xref:Microsoft.VisualStudio.VCProjectEngine.VCCLCompilerTool.AdditionalOptions%2A>」を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [リンカー オプションの設定](../../build/reference/setting-linker-options.md)   
 [リンカー オプション](../../build/reference/linker-options.md)