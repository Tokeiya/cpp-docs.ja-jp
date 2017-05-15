---
title: "CInternetSession クラス |Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CInternetSession
- AFXINET/CInternetSession
- AFXINET/CInternetSession::CInternetSession
- AFXINET/CInternetSession::Close
- AFXINET/CInternetSession::EnableStatusCallback
- AFXINET/CInternetSession::GetContext
- AFXINET/CInternetSession::GetCookie
- AFXINET/CInternetSession::GetCookieLength
- AFXINET/CInternetSession::GetFtpConnection
- AFXINET/CInternetSession::GetGopherConnection
- AFXINET/CInternetSession::GetHttpConnection
- AFXINET/CInternetSession::OnStatusCallback
- AFXINET/CInternetSession::OpenURL
- AFXINET/CInternetSession::SetCookie
- AFXINET/CInternetSession::SetOption
dev_langs:
- C++
helpviewer_keywords:
- CInternetSession class
- Internet sessions
ms.assetid: ef54feb4-9d0f-4e65-a45d-7a4cf6c40e51
caps.latest.revision: 25
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
ms.sourcegitcommit: bb94e24657d16b2a3eda3a770c2b6ae734c6006f
ms.openlocfilehash: 1bc8f21cd68741a4b0560ea3e1cb678be50dcf89
ms.lasthandoff: 04/12/2017

---
# <a name="cinternetsession-class"></a>CInternetSession クラス
単一のインターネット セッションまたは複数の同時インターネット セッションを作成し、初期化します。必要な場合は、プロキシ サーバーへの接続も記述します。  
  
## <a name="syntax"></a>構文  
  
```  
class CInternetSession : public CObject  
```  
  
## <a name="members"></a>メンバー  
  
### <a name="public-constructors"></a>パブリック コンストラクター  
  
|名前|説明|  
|----------|-----------------|  
|[CInternetSession::CInternetSession](#cinternetsession)|`CInternetSession` オブジェクトを構築します。|  
  
### <a name="public-methods"></a>パブリック メソッド  
  
|名前|説明|  
|----------|-----------------|  
|[CInternetSession::Close](#close)|インターネット セッションが終了した場合に、インターネット接続を閉じます。|  
|[CInternetSession::EnableStatusCallback](#enablestatuscallback)|ステータス コールバック ルーチンを確立します。|  
|[CInternetSession::GetContext](#getcontext)|インターネット セッションが終了した場合に、インターネット接続を閉じます。|  
|[CInternetSession::GetCookie](#getcookie)|指定した URL とそのすべての親の Url の cookie を返します。|  
|[CInternetSession::GetCookieLength](#getcookielength)|バッファーに格納されている cookie の長さを指定する変数を取得します。|  
|[CInternetSession::GetFtpConnection](#getftpconnection)|サーバーと FTP セッションを開きます。 ユーザーをログオンします。|  
|[代わり](#getgopherconnection)|Gopher サーバーは接続を開こうとしているアプリケーションを開きます。|  
|[代わりに](#gethttpconnection)|HTTP サーバーは接続を開こうとしているアプリケーションを開きます。|  
|[:Onstatuscallback](#onstatuscallback)|ステータス コールバックが有効な場合は、操作のステータスを更新します。|  
|[できます](#openurl)|解析し、URL が表示されます。|  
|[CInternetSession::SetCookie](#setcookie)|指定された URL の cookie を設定します。|  
|[CInternetSession::SetOption](#setoption)|インターネット セッションのオプションを設定します。|  
  
### <a name="public-operators"></a>パブリック演算子  
  
|名前|説明|  
|----------|-----------------|  
|[CInternetSession::operator HINTERNET](#operator_hinternet)|現在のインターネット セッションへのハンドル。|  
  
## <a name="remarks"></a>コメント  
 アプリケーションの実行中には、インターネット接続を保持する必要が場合、は、作成、`CInternetSession`クラスのメンバー [CWinApp](../../mfc/reference/cwinapp-class.md)です。  
  
 インターネット セッションを確立すると呼び出す[OpenURL](#openurl)です。 `CInternetSession`インデクサーは、URL をグローバル関数を呼び出すことによって[AfxParseURL](internet-url-parsing-globals.md#afxparseurl)です。 そのプロトコルの種類に関係なく`CInternetSession`URL を解釈しを管理します。 URL リソース file:// で識別されるローカル ファイルへの要求を処理できます。 `OpenURL`ポインターを返す、 [CStdioFile](../../mfc/reference/cstdiofile-class.md)オブジェクト名を渡す場合に、ローカル ファイルです。  
  
 使用してインターネット サーバーの URL を開くかどうか`OpenURL`、サイトから情報を読み取ることができます。 に対して、サーバー上にあるファイル (例、HTTP、FTP、または gopher) 用サービスに固有のアクションを実行する場合は、そのサーバーに適切な接続を確立する必要があります。 特定の種類の特定のサービスに直接接続を開くには、次のメンバー関数のいずれかの手順に従います。  
  
- [GetGopherConnection](#getgopherconnection) gopher サービスへの接続を開きます。  
  
- [GetHttpConnection](#gethttpconnection)を HTTP サービスへの接続を開きます。  
  
- [GetFtpConnection](#getftpconnection)を FTP サービスへの接続を開きます。  
  
 [SetOption](#setoption)タイムアウト値、再試行の回数など、セッションのクエリ オプションを設定したりすることができます。  
  
 `CInternetSession`メンバー関数[SetCookie](#setcookie)を[GetCookie](#getcookie)と[GetCookieLength](#getcookielength)使用するサーバーとスクリプトの状態に関する情報を保持クライアント ワークステーション Win32 cookie データベースを管理する手段を提供します。  
  
 インターネットの基本的なプログラミング タスクの詳細については、記事を参照してください。[インターネットの最初の手順: WinInet](../../mfc/wininet-basics.md)です。 MFC WinInet クラスの使用に関する全般情報の記事を参照してください。 [wininet の基礎を使用したプログラミング インターネット](../../mfc/win32-internet-extensions-wininet.md)です。  
  
> [!NOTE]
> `CInternetSession`スローされます、 [AfxThrowNotSupportedException](exception-processing.md#afxthrownotsupportedexception)サポートされていないサービスの種類。 次のサービス型のみが現在サポートされて: FTP、HTTP、gopher、およびファイルです。  
  
## <a name="inheritance-hierarchy"></a>継承階層  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 `CInternetSession`  
  
## <a name="requirements"></a>要件  
 **ヘッダー:** afxinet.h  
  
##  <a name="cinternetsession"></a>CInternetSession::CInternetSession  
 このメンバー関数が呼び出されます、`CInternetSession`オブジェクトを作成します。  
  
```  
CInternetSession(
    LPCTSTR pstrAgent = NULL,  
    DWORD_PTR dwContext = 1,  
    DWORD dwAccessType = PRE_CONFIG_INTERNET_ACCESS,  
    LPCTSTR pstrProxyName = NULL,  
    LPCTSTR pstrProxyBypass = NULL,  
    DWORD dwFlags = 0);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrAgent`  
 アプリケーションまたはインターネット関数 (たとえば、「Microsoft インターネット ブラウザー」) を呼び出してエンティティの名前を識別する文字列へのポインター。 場合`pstrAgent`は**NULL** (既定)、フレームワークがグローバル関数を呼び出す[AfxGetAppName](application-information-and-management.md#afxgetappname)アプリケーションの名前を表す null で終わる文字列が返されます。 一部のプロトコルでは、この文字列を使用するサーバーにアプリケーションを識別します。  
  
 `dwContext`  
 操作のコンテキストの識別子。 `dwContext`によって返される操作のステータス情報を識別する[:onstatuscallback](#onstatuscallback)です。 既定値を 1 に設定します。ただし、操作の特定のコンテキスト ID を明示的に割り当てることができます。 オブジェクトとその動作はしたコンテキスト ID と関連付けられます  
  
 `dwAccessType`  
 必要なアクセスの種類。 うち 1 つだけを指定することがあります、有効な値を次に示します。  
  
- **INTERNET_OPEN_TYPE_PRECONFIG**レジストリに事前に構成された設定を使用して接続します。 このアクセスの種類は、既定値として設定されます。 TIS プロキシを介して接続するには、設定`dwAccessType`です。 この値にするし、レジストリを適切に設定します。  
  
- `INTERNET_OPEN_TYPE_DIRECT`インターネットに直接接続します。  
  
- `INTERNET_OPEN_TYPE_PROXY`CERN プロキシ経由で接続します。  
  
 さまざまな種類のプロキシの接続の詳細については、次を参照してください。[典型的な FTP クライアント アプリケーションのステップ](../../mfc/steps-in-a-typical-ftp-client-application.md)です。  
  
 *pstrProxyName*  
 優先 CERN プロキシの名前場合`dwAccessType`として設定されている`INTERNET_OPEN_TYPE_PROXY`です。 既定値は**NULL**です。  
  
 *pstrProxyBypass*  
 サーバーのアドレスのオプションのリストを含む文字列へのポインター。 プロキシへのアクセスを使用する場合は、これらのアドレスを迂回する可能性があります。 場合、 **NULL**値が指定された場合、バイパス リストは、レジストリから読み取られます。 このパラメーターは、意味のある場合にのみ、`dwAccessType`に設定されている`INTERNET_OPEN_TYPE_PROXY`です。  
  
 `dwFlags`  
 さまざまなキャッシュ オプションを示します。 既定値は 0 に設定されます。 使用可能な値は次のとおりです。  
  
- `INTERNET_FLAG_DONT_CACHE`ローカルまたはゲートウェイ サーバーに、データをキャッシュしません。  
  
- `INTERNET_FLAG_OFFLINE`ダウンロード操作がなければ、永続的なキャッシュのみを使用します。 項目がキャッシュに存在しない場合は、該当するエラー コードが返されます。 このフラグは、ビットごとと組み合わせること`OR`( **|**) 演算子。  
  
### <a name="remarks"></a>コメント  
 **CInternetSession**は、アプリケーションによって呼び出される最初のインターネット関数。 内部データ構造体を初期化し、アプリケーションからの以降の呼び出しを準備します。  
  
 インターネット接続を開くことができる場合`CInternetSession`スロー、 [AfxThrowInternetException](internet-url-parsing-globals.md#afxthrowinternetexception)です。  
  
### <a name="example"></a>例  
  例を参照して[CFtpFileFind](../../mfc/reference/cftpfilefind-class.md)です。  
  
##  <a name="close"></a>CInternetSession::Close  
 このメンバー関数を使用して、アプリケーションが終了すると、`CInternetSession`オブジェクト。  
  
```  
virtual void Close();
```  
  
### <a name="example"></a>例  
  例を参照して[CFtpFileFind](../../mfc/reference/cftpfilefind-class.md)です。  
  
##  <a name="enablestatuscallback"></a>CInternetSession::EnableStatusCallback  
 ステータス コールバックを有効にするには、このメンバー関数を呼び出します。  
  
```  
BOOL EnableStatusCallback(BOOL bEnable = TRUE);
```  
  
### <a name="parameters"></a>パラメーター  
 `bEnable`  
 コールバックを有効または無効になっているかどうかを指定します。 既定値は**TRUE**です。  
  
### <a name="return-value"></a>戻り値  
 正常終了した場合は 0 以外を返します。それ以外の場合は 0 を返します。 呼び出しに失敗した場合は、スローされたエラーの原因を判断[CInternetException](../../mfc/reference/cinternetexception-class.md)オブジェクト。  
  
### <a name="remarks"></a>コメント  
 ステータス コールバックを処理する場合は、アプリケーションのステータス バーに (名前の解決、サーバーに接続する) などの操作の進行状況に関するステータスを提供できます。 操作のステータスの表示は、長期的な操作中に特にです。  
  
 コールバックは、要求の処理中に発生する、ためアプリケーションはネットワークにデータ スループットの低下を回避するためのコールバックで可能な時間を節約する必要があります。 たとえば、コールバックでは、ダイアログ ボックスを配置するには、時間のかかる操作サーバーは要求を終了する可能性があります。  
  
 ステータス コールバックは、いずれかのコールバックが保留になっている限り削除できません。  
  
 何らかの操作を非同期的に処理するためには、独自のスレッドを作成するか、MFC を使わない WinInet 関数を使用する必要があります。  
  
##  <a name="getcontext"></a>CInternetSession::GetContext  
 特定のアプリケーションのセッションのコンテキスト値を取得するには、このメンバー関数を呼び出します。  
  
```  
DWORD_PTR GetContext() const;  
```  
  
### <a name="return-value"></a>戻り値  
 アプリケーションで定義されたコンテキスト識別子。  
  
### <a name="remarks"></a>コメント  
 [OnStatusCallback](#onstatuscallback)によって返されるコンテキスト ID を使用して**GetContext**特定のアプリケーションの状態を報告します。 たとえば、ステータス情報を返すを含むインターネット要求をアクティブにしても、ときにステータス コールバックは、その要求にステータスをレポートするコンテキスト ID を使用しています。 2 つの個別のアクティブ化した場合は、インターネットの両方が含まれる状態情報を返すことが要求`OnStatusCallback`コンテキスト識別子を使用して、対応する要求のステータスを返します。 その結果、すべてのステータス コールバック操作のコンテキスト id を使用し、セッションが終了するまで、セッションに関連付けられています。  
  
 非同期操作の詳細については、記事を参照してください。[インターネットの最初の手順: WinInet](../../mfc/wininet-basics.md)です。  
  
##  <a name="getcookie"></a>CInternetSession::GetCookie  
 このメンバー関数は、Win32 関数の動作を実装して[InternetGetCookie](http://msdn.microsoft.com/library/windows/desktop/aa384710)で説明されている、[!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]です。  
  
```  
static BOOL GetCookie(
    LPCTSTR pstrUrl,  
    LPCTSTR pstrCookieName,  
    LPTSTR pstrCookieData,  
    DWORD dwBufLen);

 
static BOOL GetCookie(
    LPCTSTR pstrUrl,  
    LPCTSTR pstrCookieName,  
    CString& strCookieData);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrUrl`  
 URL を含む文字列へのポインター。  
  
 `pstrCookieName`  
 指定された URL を取得する cookie の名前を含む文字列へのポインター。  
  
 `pstrCookieData`  
 最初のオーバー ロードで、cookie のデータを受け取るバッファーのアドレスを表す文字列へのポインター。 この値は、 **NULL**です。 2 番目のオーバー ロードへの参照では、 [CString](../../atl-mfc-shared/reference/cstringt-class.md) cookie のデータを受信するオブジェクト。  
  
 `dwBufLen`  
 サイズを指定する、変数、`pstrCookieData`バッファー。 バッファーにコピーするデータの量に格納、関数が成功した場合、`pstrCookieData`バッファー。 場合`pstrCookieData`は**NULL**、このパラメーターは、すべての cookie のデータをコピーするために必要なバッファーのサイズを指定する値を受け取ります。  
  
### <a name="return-value"></a>戻り値  
 返します**TRUE**成功した場合、または**FALSE**それ以外の場合。 呼び出しに失敗した場合は、Win32 関数を呼び出す[GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360)エラーの原因を特定します。 次のエラー値が適用されます。  
  
- **ERROR_NO_MORE_ITEMS**指定された URL の cookie とそのすべての親はありません。  
  
- **ERROR_INSUFFICIENT_BUFFER**に渡された値`dwBufLen`cookie のすべてのデータをコピーするのに十分ではありません。 返される値`dwBufLen`バッファーのサイズをすべてのデータを取得するために必要です。  
  
### <a name="remarks"></a>コメント  
 2 番目のオーバー ロードでは、MFC、cookie にデータを取得、指定された`CString`オブジェクト。  
  
##  <a name="getcookielength"></a>CInternetSession::GetCookieLength  
 バッファーに格納されている cookie の長さを取得するには、このメンバー関数を呼び出します。  
  
```  
static DWORD GetCookieLength(
    LPCTSTR pstrUrl,  
    LPCTSTR pstrCookieName);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrUrl`  
 URL を含む文字列へのポインター  
  
 `pstrCookieName`  
 Cookie の名前を含む文字列へのポインター。  
  
### <a name="return-value"></a>戻り値  
 A`DWORD`バッファーに格納されている、cookie の長さを示す値。 によって示される名前のない cookie の場合は 0`pstrCookieName`が存在します。  
  
### <a name="remarks"></a>コメント  
 この値を使用して[GetCookie](#getcookie)です。  
  
##  <a name="getftpconnection"></a>CInternetSession::GetFtpConnection  
 FTP 接続を確立しへのポインターを取得するには、このメンバー関数を呼び出す、`CFtpConnection`オブジェクト。  
  
```  
CFtpConnection* GetFtpConnection(
    LPCTSTR pstrServer,  
    LPCTSTR pstrUserName = NULL,  
    LPCTSTR pstrPassword = NULL,  
    INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
    BOOL bPassive = FALSE);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrServer`  
 FTP サーバーの名前を含む文字列へのポインター。  
  
 `pstrUserName`  
 ログインするユーザーの名前を指定する null で終わる文字列へのポインター。 場合**NULL**、既定値は匿名です。  
  
 `pstrPassword`  
 ログインに使用するパスワードを指定する null で終わる文字列へのポインター。 両方`pstrPassword`と`pstrUserName`は**NULL**既定の匿名パスワードはユーザーの電子メール名。 場合`pstrPassword`は**NULL** (または空の文字列) が、`pstrUserName`は**NULL**を空白のパスワードを使用します。 次の表の 4 種類の設定の動作は、`pstrUserName`と`pstrPassword`:  
  
|`pstrUserName`|`pstrPassword`|FTP サーバーに送信されるユーザー名|FTP サーバーに送信されたパスワード|  
|--------------------|--------------------|---------------------------------|---------------------------------|  
|**NULL**または""|**NULL**または""|「匿名」|ユーザーの電子メール名|  
|非- **NULL**文字列|**NULL**または""|`pstrUserName`|" "|  
|**NULL**以外**NULL**文字列|**エラー**|**エラー**||  
|非- **NULL**文字列|非- **NULL**文字列|`pstrUserName`|`pstrPassword`|  
  
 `nPort`  
 サーバーで使用する TCP/IP ポートを識別する番号。  
  
 `bPassive`  
 この FTP セッションのパッシブまたはアクティブ モードを指定します。 場合に設定**TRUE**、Win32 API を設定して`dwFlag`に**INTERNET_FLAG_PASSIVE**です。  
  
### <a name="return-value"></a>戻り値  
 ポインター、 [CFtpConnection](../../mfc/reference/cftpconnection-class.md)オブジェクト。 呼び出しに失敗した場合は、スローされたエラーの原因を判断[CInternetException](../../mfc/reference/cinternetexception-class.md)オブジェクト。  
  
### <a name="remarks"></a>コメント  
 `GetFtpConnection`FTP サーバーに接続しを作成してへのポインターを返します、 **CFTPConnection**オブジェクト。 サーバー上の特定の操作は行われません。 ファイルに対する読み取りまたは書き込みする場合は、たとえば、別の手順としてこれらの操作を実行する必要があります。 クラスを参照してください[CFtpConnection](../../mfc/reference/cftpconnection-class.md)と[CFtpFileFind](../../mfc/reference/cftpfilefind-class.md)ファイルの検索方法については、のファイルを開くの読み取りや書き込みをファイルにします。 記事を参照して[wininet の基礎を使用したプログラミング インターネット](../../mfc/win32-internet-extensions-wininet.md)FTP 接続の一般的なタスクを実行する手順についてです。  
  
### <a name="example"></a>例  
  例を参照して[CFtpFileFind](../../mfc/reference/cftpfilefind-class.md)です。  
  
##  <a name="getgopherconnection"></a>代わり  
 新しい gopher 接続を確立しへのポインターを取得するには、このメンバー関数を呼び出す、`CGopherConnection`オブジェクト。  
  
```  
CGopherConnection* GetGopherConnection(
    LPCTSTR pstrServer,  
    LPCTSTR pstrUserName = NULL,  
    LPCTSTR pstrPassword = NULL,  
    INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrServer`  
 Gopher サーバー名を含む文字列へのポインター。  
  
 `pstrUserName`  
 ユーザー名を含む文字列へのポインター。  
  
 `pstrPassword`  
 アクセスのパスワードを含む文字列へのポインター。  
  
 `nPort`  
 サーバーで使用する TCP/IP ポートを識別する番号。  
  
### <a name="return-value"></a>戻り値  
 ポインター、[関数](../../mfc/reference/cgopherconnection-class.md)オブジェクト。 呼び出しに失敗した場合は、スローされたエラーの原因を判断[CInternetException](../../mfc/reference/cinternetexception-class.md)オブジェクト。  
  
### <a name="remarks"></a>コメント  
 `GetGopherConnection`gopher サーバーに接続しを作成してへのポインターを返します、`CGopherConnection`オブジェクト。 サーバー上の特定の操作は行われません。 データを読み取ったり書き込んだりする場合は、たとえば、別の手順としてこれらの操作を実行する必要があります。 クラスを参照してください[関数](../../mfc/reference/cgopherconnection-class.md)を[CGopherFile](../../mfc/reference/cgopherfile-class.md)と[CGopherFileFind](../../mfc/reference/cgopherfilefind-class.md)ファイルの検索方法については、のファイルを開くの読み取りや書き込みをファイルにします。 FTP サイトを参照する方法については、このメンバー関数を参照してください。 [OpenURL](#openurl)です。 記事を参照して[wininet の基礎を使用したプログラミング インターネット](../../mfc/win32-internet-extensions-wininet.md)gopher 接続の一般的なタスクを実行する手順についてです。  
  
##  <a name="gethttpconnection"></a>代わりに  
 HTTP 接続を確立しへのポインターを取得するには、このメンバー関数を呼び出す、`CHttpConnection`オブジェクト。  
  
```  
CHttpConnection* GetHttpConnection(
    LPCTSTR pstrServer,  
    INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
    LPCTSTR pstrUserName = NULL,  
    LPCTSTR pstrPassword = NULL);

 
CHttpConnection* GetHttpConnection(
    LPCTSTR pstrServer,  
    DWORD dwFlags,  
    INTERNET_PORT nPort = INTERNET_INVALID_PORT_NUMBER,  
    LPCTSTR pstrUserName = NULL,  
    LPCTSTR pstrPassword = NULL);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrServer`  
 HTTP サーバー名を含む文字列へのポインター。  
  
 `nPort`  
 サーバーで使用する TCP/IP ポートを識別する番号。  
  
 `pstrUserName`  
 ユーザー名を含む文字列へのポインター。  
  
 `pstrPassword`  
 アクセスのパスワードを含む文字列へのポインター。  
  
 *dwflags*  
 任意の組み合わせ、 **INTERNET_ _\***フラグ。 表を参照して、**解説**のセクション[しないで](../../mfc/reference/chttpconnection-class.md#openrequest)の詳細については`dwFlags`値。  
  
### <a name="return-value"></a>戻り値  
 ポインター、 [CHttpConnection](../../mfc/reference/chttpconnection-class.md)オブジェクト。 呼び出しに失敗した場合は、スローされたエラーの原因を判断[CInternetException](../../mfc/reference/cinternetexception-class.md)オブジェクト。  
  
### <a name="remarks"></a>コメント  
 `GetHttpConnection`HTTP サーバーに接続しを作成してへのポインターを返します、`CHttpConnection`オブジェクト。 サーバー上の特定の操作は行われません。 たとえば、HTTP ヘッダーを照会する場合は、別のステップとしてこの操作を実行する必要があります。 クラスを参照してください[CHttpConnection](../../mfc/reference/chttpconnection-class.md)と[CHttpFile](../../mfc/reference/chttpfile-class.md)操作については、HTTP サーバーへの接続を使用して実行することができます。 HTTP サイトを参照する方法については、このメンバー関数を参照してください。 [OpenURL](#openurl)です。 記事を参照して[wininet の基礎を使用したプログラミング インターネット](../../mfc/win32-internet-extensions-wininet.md)HTTP 接続の一般的なタスクを実行する手順についてです。  
  
##  <a name="onstatuscallback"></a>:Onstatuscallback  
 このメンバー関数は、ステータス コールバックが有効にし、操作が保留中の状態を更新するためにフレームワークによって呼び出されます。  
  
```  
virtual void OnStatusCallback(
    DWORD_PTR dwContext,  
    DWORD dwInternetStatus,  
    LPVOID lpvStatusInformation,  
    DWORD dwStatusInformationLength);
```  
  
### <a name="parameters"></a>パラメーター  
 `dwContext`  
 アプリケーションによって提供されるコンテキストの値です。  
  
 `dwInternetStatus`  
 コールバックが行われる理由を示すステータス コード。 参照してください**解説**可能な値のテーブルにします。  
  
 `lpvStatusInformation`  
 このコールバックに関連する情報を格納するバッファーへのポインター。  
  
 `dwStatusInformationLength`  
 `lpvStatusInformation` のサイズ。  
  
### <a name="remarks"></a>コメント  
 最初に呼び出す必要があります[使用](#enablestatuscallback)ステータス コールバックを活用するためにします。  
  
 `dwInternetStatus`パラメーターは、実行中の操作を示すしの内容を決定`lpvStatusInformation`になります。 `dwStatusInformationLength`含まれるデータの長さを示す`lpvStatusInformation`です。 次の状態の値を`dwInternetStatus`次のように定義されます。  
  
|値|説明|  
|-----------|-------------|  
|`INTERNET_STATUS_RESOLVING_NAME`|含まれている名前の IP アドレスの検索`lpvStatusInformation`です。|  
|`INTERNET_STATUS_NAME_RESOLVED`|含まれている名前の IP アドレスを正常に見つかった`lpvStatusInformation`です。|  
|`INTERNET_STATUS_CONNECTING_TO_SERVER`|ソケット アドレスへの接続 ( [SOCKADDR](../../mfc/reference/sockaddr-structure.md)) によって示される`lpvStatusInformation`です。|  
|`INTERNET_STATUS_CONNECTED_TO_SERVER`|ソケット アドレスが正常に接続されている ( `SOCKADDR`) によって示される`lpvStatusInformation`です。|  
|`INTERNET_STATUS_SENDING_REQUEST`|サーバーに情報の要求を送信します。 `lpvStatusInformation`パラメーターは**NULL**です。|  
|**INTERNET_STATUS_ REQUEST_SENT**|サーバーに情報の要求が正常に送信します。 `lpvStatusInformation`パラメーターは**NULL**です。|  
|`INTERNET_STATUS_RECEIVING_RESPONSE`|サーバーの要求に応答を待機しています。 `lpvStatusInformation`パラメーターは**NULL**です。|  
|`INTERNET_STATUS_RESPONSE_RECEIVED`|サーバーからの応答を受信しました。 `lpvStatusInformation`パラメーターは**NULL**です。|  
|`INTERNET_STATUS_CLOSING_CONNECTION`|サーバーへの接続を終了しています。 `lpvStatusInformation`パラメーターは**NULL**です。|  
|`INTERNET_STATUS_CONNECTION_CLOSED`|サーバーへの接続が正常に終了しました。 `lpvStatusInformation`パラメーターは**NULL**です。|  
|`INTERNET_STATUS_HANDLE_CREATED`|Win32 API 関数で使用される[InternetConnect](http://msdn.microsoft.com/library/windows/desktop/aa384363)新しいハンドルが作成されたことを示すためにします。 これにより、アプリケーションの呼び出し、Win32 関数[InternetCloseHandle](http://msdn.microsoft.com/library/windows/desktop/aa384350)から別のスレッドの接続の時間がかかりすぎる場合です。 参照してください、[!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]詳細については、これらの関数。|  
|`INTERNET_STATUS_HANDLE_CLOSING`|このハンドルの値が正常に終了します。|  
  
 ステータス コールバック ルーチンが実行される前に、何らかのアクションを要求するには、このメンバー関数をオーバーライドします。  
  
> [!NOTE]
>  ステータス コールバックには、スレッド状態の保護が必要があります。 MFC の共有ライブラリを使用している場合は、オーバーライドの先頭に次の行を追加します。  
  
 [!code-cpp[NVC_MFCHtmlHttp #8](../../mfc/reference/codesnippet/cpp/cinternetsession-class_1.cpp)]  
  
 非同期操作の詳細については、記事を参照してください。[インターネットの最初の手順: WinInet](../../mfc/wininet-basics.md)です。  
  
##  <a name="openurl"></a>できます  
 HTTP サーバーに指定された要求を送信し、MIME 追加 RFC822 を指定するクライアントを許可するには、関数、または、要求と共に送信する HTTP ヘッダーは、このメンバーを呼び出します。  
  
```  
CStdioFile* OpenURL(
    LPCTSTR pstrURL,  
    DWORD_PTR dwContext = 1,  
    DWORD dwFlags = INTERNET_FLAG_TRANSFER_ASCII,  
    LPCTSTR pstrHeaders = NULL,  
    DWORD dwHeadersLength = 0);
```  
  
### <a name="parameters"></a>パラメーター  
 *pstrURL*  
 読み取りを開始する URL の名前へのポインター。 Url のみファイルで始まる: ftp: gopher: または http: はサポートされています。 **アサート**場合*pszURL*は**NULL**です。  
  
 `dwContext`  
 コールバックに返されるハンドルを使用して、アプリケーション定義の値が渡されます。  
  
 `dwFlags`  
 この接続を処理する方法を示すフラグ。 参照してください**解説**詳細については、有効なフラグです。 有効なフラグは次のとおりです。  
  
- **INTERNET_FLAG_TRANSFER_ASCII**既定値です。 ASCII テキストとしてファイルを転送します。  
  
- **INTERNET_FLAG_TRANSFER_BINARY**バイナリ ファイルとしてファイルを転送します。  
  
- `INTERNET_FLAG_RELOAD`ローカルにキャッシュされている場合でも、ネットワークからデータを取得します。  
  
- `INTERNET_FLAG_DONT_CACHE`ローカルまたはすべてのゲートウェイに、データをキャッシュしません。  
  
- `INTERNET_FLAG_SECURE`このフラグは、HTTP 要求のみに適用します。 セキュア ソケット レイヤーまたは割合で、ネットワーク上でセキュリティ保護されたトランザクションを要求します。  
  
- **INTERNET_OPEN_FLAG_USE_EXISTING_CONNECT**によって生成される新しい要求をサーバーに既存の接続を再利用可能であれば、 **OpenUrl**接続要求ごとに新しいセッションを作成する代わりにします。  
  
- **INTERNET_FLAG_PASSIVE** FTP サイトに使用します。 パッシブ FTP を使用します。 と共に使用[関数](../../mfc/reference/cinternetconnection-class.md)の`OpenURL`します。  
  
 `pstrHeaders`  
 HTTP サーバーに送信されるヘッダーを含む文字列へのポインター。  
  
 *dwHeadersLength*  
 追加のヘッダーの文字の長さ。 場合は-1 L と`pstrHeaders`以外**NULL**、し`pstrHeaders`を 0 にするには、終了され、長さは、計算と見なされます。  
  
### <a name="return-value"></a>戻り値  
 FTP、GOPHER、HTTP、およびファイルの種類のインターネット サービスのみのファイル ハンドルを返します。 返します**NULL**解析が成功した場合。  
  
 マウス ポインターを`OpenURL`を返しますが異なります*pszURL*のサービスの種類。 次の表は、可能なポインターを示しています。`OpenURL`返すことができます。  
  
|URL の種類|戻り値|  
|--------------|-------------|  
|file://|**CStdioFile\***|  
|http://|**CHttpFile\***|  
|gopher://|**CGopherFile\***|  
|ftp://|**CInternetFile\***|  
  
### <a name="remarks"></a>コメント  
 パラメーター`dwFlags`いずれかを含める必要があります**INTERNET_FLAG_TRANSFER_ASCII**または**INTERNET_FLAG_TRANSFER_BINARY**、両方は使用しません。 その他のフラグは、演算と組み合わせることができます`OR`演算子 ( **|**)。  
  
 `OpenURL`、Win32 関数をラップする**アクセス**、により、のみをダウンロード、取得、およびインターネット サーバーからデータを読み取るします。 `OpenURL`により、なし、リモートの場所にファイルの操作に必要のないように[関数](../../mfc/reference/cinternetconnection-class.md)オブジェクト。  
  
 特定の接続を使用する (つまり、プロトコル固有) 関数などのファイルに書き込み、する必要がありますセッションを開く特定の種類の接続を開くし、その接続を使用して、目的のモードでファイルを開きます。 参照してください`CInternetConnection`接続に固有の機能についての詳細。  
  
##  <a name="operator_hinternet"></a>CInternetSession::operator HINTERNET  
 この演算子を使用して、現在のインターネット セッションの Windows ハンドルを取得します。  
  
```  
operator HINTERNET() const;  
```  
  
##  <a name="setcookie"></a>CInternetSession::SetCookie  
 指定された URL の cookie を設定します。  
  
```  
static BOOL SetCookie(
    LPCTSTR pstrUrl,  
    LPCTSTR pstrCookieName,  
    LPCTSTR pstrCookieData);
```  
  
### <a name="parameters"></a>パラメーター  
 `pstrUrl`  
 Cookie を設定する URL を指定する null で終わる文字列へのポインター。  
  
 `pstrCookieName`  
 Cookie の名前を含む文字列へのポインター。  
  
 `pstrCookieData`  
 URL に関連付けるを実際の文字列データを含む文字列へのポインター。  
  
### <a name="return-value"></a>戻り値  
 返します**TRUE**成功した場合、または**FALSE**それ以外の場合。 特定のエラー コードを取得するには、呼び出す**GetLastError です。**  
  
### <a name="remarks"></a>コメント  
 このメンバー関数は、Win32 メッセージの動作を実装して[InternetSetCookie](http://msdn.microsoft.com/library/windows/desktop/aa385107)で説明されている、[!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]です。  
  
##  <a name="setoption"></a>CInternetSession::SetOption  
 インターネット セッションのオプションを設定するには、このメンバー関数を呼び出します。  
  
```  
BOOL SetOption(
    DWORD dwOption,  
    LPVOID lpBuffer,  
    DWORD dwBufferLength,  
    DWORD dwFlags = 0);

 
BOOL SetOption(
    DWORD dwOption,  
    DWORD dwValue,  
    DWORD dwFlags = 0);
```  
  
### <a name="parameters"></a>パラメーター  
 `dwOption`  
 インターネット オプションを設定します。 参照してください[オプション フラグ](http://msdn.microsoft.com/library/windows/desktop/aa385328)で、[!INCLUDE[winSDK](../../atl/includes/winsdk_md.md)]使用可能なオプションの一覧についてはします。  
  
 `lpBuffer`  
 オプションの設定を格納するバッファー。  
  
 *dwBufferLength*  
 長さ`lpBuffer`のサイズまたは`dwValue`です。  
  
 `dwValue`  
 A`DWORD`オプションの設定を格納しています。  
  
 `dwFlags`  
 さまざまなキャッシュ オプションを示します。 既定値は 0 に設定されます。 使用可能な値は次のとおりです。  
  
- `INTERNET_FLAG_DONT_CACHE`ローカルまたはゲートウェイ サーバーに、データをキャッシュしません。  
  
- `INTERNET_FLAG_OFFLINE`ダウンロード操作がなければ、永続的なキャッシュのみを使用します。 項目がキャッシュに存在しない場合は、該当するエラー コードが返されます。 このフラグは、ビットごとと組み合わせること`OR`( **|**) 演算子。  
  
### <a name="return-value"></a>戻り値  
 操作が成功した場合の値**TRUE**が返されます。 エラーが発生しました、値の場合**FALSE**が返されます。 呼び出しが失敗した場合は、Win32 関数[GetLastError](http://msdn.microsoft.com/library/windows/desktop/ms679360)エラーの原因を特定するのに呼び出せる可能性があります。  
  
## <a name="see-also"></a>関連項目  
 [CObject クラス](../../mfc/reference/cobject-class.md)   
 [階層図](../../mfc/hierarchy-chart.md)   
 [関数クラス](../../mfc/reference/cinternetconnection-class.md)   
 [CHttpConnection クラス](../../mfc/reference/chttpconnection-class.md)   
 [CFtpConnection クラス](../../mfc/reference/cftpconnection-class.md)   
 [CGopherConnection クラス](../../mfc/reference/cgopherconnection-class.md)
