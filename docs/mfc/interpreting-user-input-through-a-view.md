---
title: "ビューを経由したユーザー入力の解釈 | Microsoft Docs"
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
  - "CView クラス, 解釈 (ユーザー入力を)"
  - "入力, ビュー クラス"
  - "解釈 (ビューを通じてユーザー入力を)"
  - "ユーザー入力, 解釈 (ビュー クラスを通じた)"
  - "ビュー, ユーザー インターフェイスと入力"
ms.assetid: f0302a70-661f-4781-8fe7-78f082bef2a5
caps.latest.revision: 9
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 5
---
# ビューを経由したユーザー入力の解釈
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

ビューのメンバー関数は、すべてのユーザー入力を処理し、復号化します。  通常、処理するビュー クラスのメッセージ ハンドラー メンバー関数を定義する:  
  
-   マウスおよびキー操作で生成された Windows [メッセージ](../mfc/messages.md)。  
  
-   メニュー、ツール バー ボタンとアクセラレータ キーの[コマンド](../mfc/user-interface-objects-and-command-ids.md)。  
  
 これらのメッセージ ハンドラー メンバー関数はデータの移動がデータ入力、選択、クリップボードに対する編集として、次の操作を理解する:  
  
-   マウスをクリックし、ドラッグおよびダブルクリック  
  
-   キーストローク  
  
-   メニュー コマンド  
  
 任意の Windows メッセージを処理するかどうかは、アプリケーションでの必要性に応じて。  
  
 [メッセージの処理とマップ"](../mfc/message-handling-and-mapping.md) は コマンドのメニュー項目やそのほかのユーザー インターフェイス オブジェクトを割り当てる方法と、ハンドラー関数にバインドする方法について説明します。  [メッセージの処理とマップ"](../mfc/message-handling-and-mapping.md) は MFC がコマンドをどのようにルーティングする方法と、それらのハンドラーを含むオブジェクトまたはに標準 Windows メッセージを送信します。  
  
 たとえば、アプリケーションでは、ビューの直接マウス描画を実装する必要がある場合があります。  Scribble サンプルは、`WM_LBUTTONDOWN``WM_MOUSEMOVE`と線分を描画するために、続行するには、終了するに `WM_LBUTTONUP` メッセージを個別に処理する方法について説明します。  一方、選択肢として、ビューのマウス クリックを解釈する必要がある場合があります。  ビューの `OnLButtonDown` のハンドラー関数は、ユーザーが描画または選択したかどうかを判定します。  オンの場合、ハンドラーはクリックがビュー オブジェクトの境界内にあり、そのときに選択された状態にオブジェクトを表示する表示を変更するかどうかを判定します。  
  
 ビューは、クリップボードの使用、編集メニューの切り取りのような特定のメニュー コマンドを、処理するか選択されたデータをコピー、貼り付け、削除します。  このようなハンドラーがクリップボードに\/から選択した項目を転送するクラス `CWnd` のクリップボード関連のメンバー関数の一部を呼び出します。  
  
## 参照  
 [ビューの使い方](../mfc/using-views.md)