---
title: "context_unblock_unbalanced クラス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- context_unblock_unbalanced
- CONCRT/concurrency::context_unblock_unbalanced
- CONCRT/concurrency::context_unblock_unbalanced::context_unblock_unbalanced
dev_langs: C++
helpviewer_keywords: context_unblock_unbalanced class
ms.assetid: a76066c8-19dd-44fa-959a-6941ec1b0d2d
caps.latest.revision: "20"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.openlocfilehash: 45121b3dba14e5672333debf364f5aea2e3e3cd5
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2017
---
# <a name="contextunblockunbalanced-class"></a>context_unblock_unbalanced クラス
このクラスは、`Block` オブジェクトの `Unblock` メソッドと `Context` メソッドの呼び出しが正しく対になっていない場合にスローされる例外を表します。  
  
## <a name="syntax"></a>構文  
  
```  
class context_unblock_unbalanced : public std::exception;  
```  
  
## <a name="members"></a>メンバー  
  
### <a name="public-constructors"></a>パブリック コンストラクター  
  
|名前|説明|  
|----------|-----------------|  
|[context_unblock_unbalanced](#ctor)|オーバーロードされます。 `context_unblock_unbalanced` オブジェクトを構築します。|  
  
## <a name="remarks"></a>コメント  
 呼び出し、`Block`と`Unblock`のメソッド、`Context`オブジェクトのペアを正しく常にする必要があります。 同時実行ランタイムでは、任意の順序で発生する操作を許可します。 呼び出しなど、`Block`への呼び出しを続けて`Unblock`、またはその逆です。 呼び出す 2 つのインスタンスの場合は、この例外がスローされます、`Unblock`メソッドで発生した行で、`Context`ブロックされていないオブジェクトです。  
  
## <a name="inheritance-hierarchy"></a>継承階層  
 `exception`  
  
 `context_unblock_unbalanced`  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** concrt.h  
  
 **名前空間:** concurrency  
  
##  <a name="ctor"></a>context_unblock_unbalanced 

 `context_unblock_unbalanced` オブジェクトを構築します。  
  
```  
explicit _CRTIMP context_unblock_unbalanced(_In_z_ const char* _Message) throw();

 
context_unblock_unbalanced() throw();
```  
  
### <a name="parameters"></a>パラメーター  
 `_Message`  
 エラーの説明メッセージ。  
  
## <a name="see-also"></a>関連項目  
 [concurrency 名前空間](concurrency-namespace.md)
