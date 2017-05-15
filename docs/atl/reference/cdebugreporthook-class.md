---
title: "CDebugReportHook クラス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CDebugReportHook
- ATLUTIL/ATL::CDebugReportHook
- ATLUTIL/ATL::CDebugReportHook::CDebugReportHook
- ATLUTIL/ATL::CDebugReportHook::CDebugReportHookProc
- ATLUTIL/ATL::CDebugReportHook::RemoveHook
- ATLUTIL/ATL::CDebugReportHook::SetHook
- ATLUTIL/ATL::CDebugReportHook::SetPipeName
- ATLUTIL/ATL::CDebugReportHook::SetTimeout
dev_langs:
- C++
helpviewer_keywords:
- CDebugReportHook class
ms.assetid: 798076c3-6e63-4286-83b8-aa1bbcd0c20c
caps.latest.revision: 22
author: mikeblome
ms.author: mblome
manager: ghogen
translation.priority.ht:
- cs-cz
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- pl-pl
- pt-br
- ru-ru
- tr-tr
- zh-cn
- zh-tw
translationtype: Machine Translation
ms.sourcegitcommit: d2d39abf526a58b8442107b5ee816f316ae841f5
ms.openlocfilehash: 1de883341e0a53a1520fa44d99e7907ee1fe10b6
ms.lasthandoff: 03/31/2017

---
# <a name="cdebugreporthook-class"></a>CDebugReportHook クラス
このクラスを使用すると、名前付きパイプにデバッグ レポートを送信します。  
  
## <a name="syntax"></a>構文  
  
```
class CDebugReportHook
```  
  
## <a name="members"></a>メンバー  
  
### <a name="public-constructors"></a>パブリック コンストラクター  
  
|名前|説明|  
|----------|-----------------|  
|[CDebugReportHook::CDebugReportHook](#cdebugreporthook)|呼び出し[SetPipeName](#setpipename)、 [SetTimeout](#settimeout)、および[SetHook](#sethook)です。|  
|[CDebugReportHook:: ~ CDebugReportHook](#dtor)|呼び出し[CDebugReportHook::RemoveHook](#removehook)です。|  
  
### <a name="public-methods"></a>パブリック メソッド  
  
|名前|説明|  
|----------|-----------------|  
|[CDebugReportHook::CDebugReportHookProc](#cdebugreporthookproc)|(静的)C ランタイム デバッグ レポート プロセスにフックされているカスタム レポート関数。|  
|[CDebugReportHook::RemoveHook](#removehook)|名前付きパイプへデバッグ レポートの送信を停止するには、このメソッドを呼び出すし、以前のレポート用のフックを復元します。|  
|[CDebugReportHook::SetHook](#sethook)|名前付きパイプにデバッグ レポートを送信を開始するには、このメソッドを呼び出します。|  
|[CDebugReportHook::SetPipeName](#setpipename)|このメソッドを呼び出してデバッグ レポートを送信するパイプの名前とコンピューターを設定します。|  
|[CDebugReportHook::SetTimeout](#settimeout)|このクラスが使用可能になる名前付きパイプの待機するミリ秒単位で時間を設定するには、このメソッドを呼び出します。|  
  
## <a name="remarks"></a>コメント  
 サービスまたは名前付きパイプにデバッグ レポートを送信するアプリケーションのデバッグ ビルドでこのクラスのインスタンスを作成します。 デバッグを呼び出すことによって生成された報告[_CrtDbgReport](../../c-runtime-library/reference/crtdbgreport-crtdbgreportw.md)またはなど、この関数のラッパーを使用して、 [ATLTRACE](debugging-and-error-reporting-macros.md#atltrace)と[ATLASSERT](debugging-and-error-reporting-macros.md#atlassert)マクロです。  
  
 このクラスを使用すると、非対話型実行されるコンポーネントを対話的にデバッグすることができます[ウィンドウ ステーション](http://msdn.microsoft.com/library/windows/desktop/ms687096)です。  
  
 スレッドの基になるセキュリティ コンテキストを使用してデバッグ レポートを送信することに注意してください。 ここで低い特権のユーザーの権限の借用が行われてなどの web アプリケーションでの状況でデバッグ レポートを表示するように、権限借用が一時的に無効にします。  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** atlutil.h  
  
##  <a name="cdebugreporthook"></a>CDebugReportHook::CDebugReportHook  
 呼び出し[SetPipeName](#setpipename)、 [SetTimeout](#settimeout)、および[SetHook](#sethook)です。  
  
```
CDebugReportHook(
    LPCSTR szMachineName = ".",
    LPCSTR szPipeName = "AtlsDbgPipe",
    DWORD dwTimeout = 20000) throw();
```  
  
### <a name="parameters"></a>パラメーター  
 `szMachineName`  
 デバッグ出力の送信先となるコンピューターの名前。 既定値は、ローカル コンピューターです。  
  
 `szPipeName`  
 デバッグ出力の送信先となる名前付きパイプの名前。  
  
 `dwTimeout`  
 このクラスが使用可能になる名前付きパイプの待機するミリ秒単位の時間。  
  
##  <a name="dtor"></a>CDebugReportHook:: ~ CDebugReportHook  
 呼び出し[CDebugReportHook::RemoveHook](#removehook)です。  
  
```
~CDebugReportHook() throw();
```  
  
##  <a name="cdebugreporthookproc"></a>CDebugReportHook::CDebugReportHookProc  
 C ランタイム デバッグ レポート プロセスにフックされているカスタム レポート関数。  
  
```
static int __cdecl CDebugReportHookProc(
    int reportType,
    char* message,
    int* returnValue) throw();
```  
  
### <a name="parameters"></a>パラメーター  
 `reportType`  
 レポート (前述、_CRT_ERROR、または _CRT_ASSERT) の型。  
  
 `message`  
 メッセージ文字列。  
  
 *戻り値*  
 によって返される値[_CrtDbgReport](../../c-runtime-library/reference/crtdbgreport-crtdbgreportw.md)です。  
  
### <a name="return-value"></a>戻り値  
 かどうか、フックでメッセージを完全に処理できるように、さらに報告する必要はありませんは、FALSE を返します。 場合に TRUE を返します`_CrtDbgReport`通常の方法でメッセージを報告する必要があります。  
  
### <a name="remarks"></a>コメント  
 レポートの関数は、名前付きパイプを開き、もう一方の端のプロセスとの通信を試みます。 パイプがビジー状態の場合、レポート機能はパイプが無料か、タイムアウト時間が経過するまで待機します。 コンス トラクターまたはへの呼び出しによって、タイムアウトを設定することができます[CDebugReportHook::SetTimeout](#settimeout)です。  
  
 呼び出し元のスレッドの基になるセキュリティ コンテキストでこの関数のコードが実行され、この関数の実行中、権限借用は、無効になっています。  
  
##  <a name="removehook"></a>CDebugReportHook::RemoveHook  
 名前付きパイプへデバッグ レポートの送信を停止するには、このメソッドを呼び出すし、以前のレポート用のフックを復元します。  
  
```
void RemoveHook() throw();
```  
  
### <a name="remarks"></a>コメント  
 呼び出し[_CrtSetReportHook2](../../c-runtime-library/reference/crtsetreporthook2-crtsetreporthookw2.md)を以前のレポート用のフックを復元します。  
  
##  <a name="sethook"></a>CDebugReportHook::SetHook  
 名前付きパイプにデバッグ レポートを送信を開始するには、このメソッドを呼び出します。  
  
```
void SetHook() throw();
```  
  
### <a name="remarks"></a>コメント  
 呼び出し[_CrtSetReportHook2](../../c-runtime-library/reference/crtsetreporthook2-crtsetreporthookw2.md)デバッグ レポートを経由してルーティング[CDebugReportHookProc](#cdebugreporthookproc)名前付きパイプにします。 このクラスの追跡、前のレポート用のフックできるように、復元時に[RemoveHook](#removehook)と呼びます。  
  
##  <a name="setpipename"></a>CDebugReportHook::SetPipeName  
 このメソッドを呼び出してデバッグ レポートを送信するパイプの名前とコンピューターを設定します。  
  
```
BOOL SetPipeName(
    LPCSTR szMachineName = ".",
    LPCSTR szPipeName = "AtlsDbgPipe") throw();
```  
  
### <a name="parameters"></a>パラメーター  
 `szMachineName`  
 デバッグ出力の送信先となるコンピューターの名前。  
  
 `szPipeName`  
 デバッグ出力の送信先となる名前付きパイプの名前。  
  
### <a name="return-value"></a>戻り値  
 成功した場合、TRUE を返しますエラー発生時に false を指定します。  
  
##  <a name="settimeout"></a>CDebugReportHook::SetTimeout  
 このクラスが使用可能になる名前付きパイプの待機するミリ秒単位で時間を設定するには、このメソッドを呼び出します。  
  
```
void SetTimeout(DWORD dwTimeout);
```  
  
### <a name="parameters"></a>パラメーター  
 `dwTimeout`  
 このクラスが使用可能になる名前付きパイプの待機するミリ秒単位の時間。  
  
## <a name="see-also"></a>関連項目  
 [クラス](../../atl/reference/atl-classes.md)
