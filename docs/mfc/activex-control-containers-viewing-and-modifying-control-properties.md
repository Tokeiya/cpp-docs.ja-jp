---
title: "ActiveX コントロール コンテナー: を表示して、コントロールのプロパティを変更する |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- properties [MFC], viewing and modifying
- ActiveX control containers [MFC], viewing and modifying properties
- resource editors, viewing and modifying ActiveX controls
- ActiveX controls [MFC], properties
- controls [MFC], properties
ms.assetid: 14ce5152-742b-4e0d-a9ab-c7b456e32918
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 90e866d1a3be4600b3b98e542caff6ed793f4226
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="activex-control-containers-viewing-and-modifying-control-properties"></a>ActiveX コントロール コンテナー : コントロール プロパティの表示と変更
プロジェクトに ActiveX コントロールを挿入するときは、表示および ActiveX コントロールでサポートされるプロパティを変更すると便利です。 この記事では、これを行う Visual C リソース エディターを使用する方法について説明します。  
  
 ActiveX コントロール コンテナー アプリケーションでは、埋め込まれたコントロールを使用する場合は、表示およびリソース エディターで、コントロールのプロパティを変更できます。 リソース エディターを使用して、デザイン時にプロパティの値を設定することができますも。 リソース エディターは、プロジェクトのリソース ファイルに、これらの値を自動的に保存します。 これらの値に初期化されるプロパティがコントロールの任意のインスタンスになります。  
  
 この手順では、プロジェクトにコントロールを挿入したと仮定します。 詳細については、次を参照してください。 [ActiveX コントロール コンテナー: コントロール コンテナー アプリケーションへのコントロールを挿入する](../mfc/inserting-a-control-into-a-control-container-application.md)です。  
  
 コントロールのプロパティを表示する最初の手順では、プロジェクトのダイアログ テンプレートに、コントロールのインスタンスを追加します。  
  
### <a name="to-view-the-properties-of-a-control"></a>コントロールのプロパティを表示するには  
  
1.  リソース ビューで、開く、**ダイアログ**フォルダーです。  
  
2.  メイン ダイアログ ボックス テンプレートを開きます。  
  
3.  ActiveX コントロールを使用して、挿入、 **ActiveX コントロールの挿入** ダイアログ ボックス。 詳細については、次を参照してください。[表示と ActiveX コントロール ダイアログ ボックスを追加する](../windows/viewing-and-adding-activex-controls-to-a-dialog-box.md)です。  
  
4.  ダイアログ ボックスで、ActiveX コントロールを選択します。  
  
5.  [プロパティ] ウィンドウからをクリックして、**プロパティ**ボタンをクリックします。  
  
 使用して、**プロパティ** ダイアログ ボックスを変更し、すぐに新しいプロパティをテストします。  
  
## <a name="see-also"></a>関連項目  
 [ActiveX コントロール コンテナー](../mfc/activex-control-containers.md)

