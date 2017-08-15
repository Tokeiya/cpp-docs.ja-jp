---
title: "チュートリアル: コマンド ラインでの C プログラムのコンパイル | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "get-started-article"
helpviewer_keywords: 
  - "C プログラムのコンパイル [C++]"
  - "コマンド ライン アプリケーション [C++], C プログラム"
  - "コンパイル (プログラムを) [C++]"
  - "Visual C, コンパイル"
ms.assetid: 7e74cc2d-54b1-49de-b7ad-d3ae6b39ab8d
caps.latest.revision: 46
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 31
---
# チュートリアル: コマンド ラインでの C プログラムのコンパイル
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

[!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] に含まれる C コンパイラを使用して、基本的なコンソール プログラムから Windows デスクトップ アプリケーションまで、あらゆるものを作成できます。  
  
 このチュートリアルでは、テキスト エディターを使用して基本的な C プログラムを作成し、それをコマンド ラインでコンパイルする方法について説明します。  
  
 このチュートリアルで示すサンプル プログラムを入力する代わりに、独自の C プログラムを使用してもかまいません。  また、ヘルプ トピックに含まれる任意の C コード サンプル プログラムを使用することもできます。  
  
 既定では、Visual C\+\+ コンパイラは .c で終わるファイルをすべて C ソース コードとして扱い、.cpp で終わるファイルをすべて C\+\+ ソース コードとして扱います。  ファイル名拡張子に関係なくコンパイラがすべてのファイルを C として扱うように強制するには、[\/Tc](../build/reference/tc-tp-tc-tp-specify-source-file-type.md) コンパイラ オプションを使用します。  
  
## 必須コンポーネント  
 C 言語の基本を理解している必要があります。  
  
### C ソース ファイルを作成してコマンド ラインでコンパイルするには  
  
1.  開発者コマンド プロンプトを開きます。  Windows 8 の **\[スタート\]** 画面で、**\[Visual Studio ツール\]** フォルダーを開いて、**\[開発者コマンド プロンプト\]** ショートカットを選択します。  これ以前のバージョンの Windows の場合は、**\[スタート\]** ボタンをクリックし、**\[すべてのプログラム\]**、**\[Microsoft Visual Studio\]**、**\[Visual Studio ツール\]** の順にクリックして、**\[開発者コマンド プロンプト\]** をクリックします。  
  
     以下の手順に従って作成するアプリケーションを正常にビルドおよび実行するために、コンピューターの Windows のバージョンおよびシステム セキュリティ構成に応じて、**\[開発者コマンド プロンプト\]** のショートカット メニューを開き、**\[管理者として実行\]** をクリックする操作が必要になる場合があります。  
  
    > [!NOTE]
    >  **\[開発者コマンド プロンプト\]** により、C コンパイラと必要なライブラリへの正しいパスが自動的に設定されます。  通常のコマンド プロンプト ウィンドウではなく、このコマンド プロンプトを使用します。  詳細については、「[コマンド ライン ビルドのパスと環境変数の設定](../build/setting-the-path-and-environment-variables-for-command-line-builds.md)」を参照してください。  
  
2.  コマンド プロンプトで、ソース ファイルのディレクトリを作成し、現在の作業ディレクトリにします。  たとえば、「**md c:\\simple**」と入力して Enter キーを押すと、simple という名前のディレクトリが作成され、その後、「**cd c:\\simple**」と入力して Enter キーを押すと、そのディレクトリに切り替わります。  
  
3.  コマンド プロンプトで「**notepad**」と入力し、Enter キーを押します。  
  
4.  メモ帳で、次の行を入力します。  
  
     [!code-cpp[NVC_Walkthrough_Compile_C#100](../build/codesnippet/CPP/walkthrough-compile-a-c-program-on-the-command-line_1.c)]  
  
5.  メニュー バーで **\[ファイル\]**、**\[保存\]** の順にクリックし、**\[名前を付けて保存\]** ダイアログ ボックスを開きます。  作成したディレクトリに移動します。  **\[ファイル名\]** ボックスにソース ファイルの名前 \(「simple.c」など\) を入力し、**\[保存の種類\]** ドロップダウン リストで **\[すべてのファイル \(\*.\*\)\]** をクリックします。  **\[保存\]** をクリックして、作業ディレクトリに C ソース ファイルを作成します。  
  
6.  コマンド プロンプトで、「**dir**」と入力し、Enter キーを押します。  作成したソース ファイルが以下のように表示されます。  
  
  **C:\\simple\>dir**  
 **ドライブ C のボリュームにラベルはありません。  ボリューム シリアル番号は CC62\-6545 です。**  
 **C:\\simple のディレクトリ**  
**10\/02\/2012  03:46 PM    \<DIR\>          .  10\/02\/2012  03:46 PM    \<DIR\>          ..  10\/02\/2012  03:36 PM               102 simple.c**  
 **1 個のファイル      102 バイト**  
 **2 個のディレクトリ  514,900,566,016 バイトの空き領域**      詳細はご使用のコンピューターによって異なります。  ソース コード ファイルが表示されない場合は、作成したディレクトリに切り替えたことを確認し、そのディレクトリに .c というファイル名拡張子でソース ファイルを保存したことを確認してください。  
  
7.  コマンド プロンプトで、**cl** コマンドをソース ファイルの名前 \(「**cl simple.c**」など\) と共に指定し、Enter キーを押してプログラムをコンパイルします。  cl.exe コンパイラは、コンパイルされたコードを含む .obj ファイルを生成してから、リンカーを実行してソース ファイル名に .exe ファイル名拡張子が付いた実行可能プログラムをビルドします \(例: simple.exe\)。  
  
     実行可能プログラムの名前は、コンパイラによって表示される出力情報の行に示されます。  
  
     **出力**  
  
  **Microsoft \(R\) C\/C\+\+ Optimizing Compiler Version 17.00.50727.1 for x86**  
**Copyright\(C\) Microsoft Corporation.  All rights reserved.  simple.c**  
**Microsoft \(R\) Incremental Linker Version 11.00.50727.1**  
**Copyright\(C\) Microsoft Corporation.  All rights reserved.  \/out:simple.exe**  
**simple.obj**      ツールのバージョン番号は、[!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] のバージョンおよびインストールした更新によって異なります。  
  
    > [!NOTE]
    >  「'cl' は、内部コマンドまたは外部コマンド、操作可能なプログラムまたはバッチ ファイルとして認識されていません」のようなエラー \(エラー C1034 またはエラー LNK1104\) を受け取った場合は、コンパイラおよびツール用に環境を設定する必要があります。  詳細については、ステップ 1 を確認してください。  
    >   
    >  コンパイラ エラーか警告を受け取った場合は、ソース コード内のエラーを調べてから保存し、コンパイラを再実行してください。  特定のエラーの詳細については、このページの検索ボックスをご利用ください。  
  
8.  プログラムを実行するには、ファイル名拡張子を指定せずその名前を入力し \(例: **simple**\)、Enter キーを押します。  
  
     プログラムは、次のテキストを表示して終了します。  
  
     `This is a native C program.`  
  
## 参照  
 [チュートリアル: Win32 コンソール プログラムの作成 \(C\+\+\)](../windows/walkthrough-creating-a-standard-cpp-program-cpp.md)   
 [C 言語リファレンス](../Topic/C%20Language%20Reference.md)   
 [C\/C\+\+ プログラムのビルド](../build/building-c-cpp-programs.md)   
 [互換性](../c-runtime-library/compatibility.md)