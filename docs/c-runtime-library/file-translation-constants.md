---
title: "ファイル変換定数 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: c.constants.file
dev_langs: C++
helpviewer_keywords:
- translation constants
- file translation [C++], constants
- translation, file translation constants
- translation, constants
- constants [C++], file translation mode
- file translation [C++]
ms.assetid: 49b13bf3-442e-4d19-878b-bd1029fa666a
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: a68c41793ea96a840a78e76e5b2a222f0b06a583
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="file-translation-constants"></a>ファイル変換定数
## <a name="syntax"></a>構文  
  
```  
  
#include <stdio.h>  
```  
  
## <a name="remarks"></a>コメント  
 これらの定数は、変換モードを指定します (**"b"** または **"t"**)。 このモードは、アクセスの種類 (**"r"**、**"w"**、**"a"**、**"r+"**、**"w+"**、**"a+"**) を指定する文字列に含まれます。  
  
 変換モードは次のとおりです。  
  
 **t**  
 テキスト (変換) モードで開きます。 このモードでは、復帰と改行 (CR-LF) の組み合わせは入力時に 1 つの改行 (LF) 文字に変換され、LF 文字は出力時に CR-LF の組み合わせに変換されます。 また、Ctrl + Z は入力時に EOF (end-of-file) 文字として解釈されます。 読み取り用または読み取り/書き込み用にファイルを開いた場合、`fopen` はファイルの終端に Ctrl + Z があるかどうかを確認し、それを削除できる場合は削除します。 この処理が行われる理由は、CTRL+Z で終わるファイルの中身を `fseek` 関数および `ftell` 関数で移動するとき、ファイル末尾付近で `fseek` が正しく動作しないことがあるためです。  
  
> [!NOTE]
>  **t** のオプションは、`fopen` と `freopen` の ANSI 標準の一部ではありません。 これは Microsoft 拡張機能です。ANSI 互換が必要な場合は使用しないでください。  
  
 **b**  
 バイナリ (無変換) モードで開きます。 上の変換は行われません。  
  
 **t** または **b** を *mode* に指定しない場合、変換モードは既定のモード変数 [_fmode](../c-runtime-library/fmode.md) によって定義されます。 テキスト モードとバイナリ モードの使用の詳細については、「[テキスト モードとバイナリ モードのファイル入出力](../c-runtime-library/text-and-binary-mode-file-i-o.md)」をご覧ください。  
  
## <a name="see-also"></a>関連項目  
 [_fdopen、_wfdopen](../c-runtime-library/reference/fdopen-wfdopen.md)   
 [fopen、_wfopen](../c-runtime-library/reference/fopen-wfopen.md)   
 [freopen、_wfreopen](../c-runtime-library/reference/freopen-wfreopen.md)   
 [_fsopen、_wfsopen](../c-runtime-library/reference/fsopen-wfsopen.md)   
 [グローバル定数](../c-runtime-library/global-constants.md)