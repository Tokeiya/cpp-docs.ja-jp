---
title: "_execlpe、_wexeclpe | Microsoft ドキュメント"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _execlpe
- _wexeclpe
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-process-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _wexeclpe
- execlpe
- wexeclpe
- _execlpe
dev_langs:
- C++
helpviewer_keywords:
- wexeclpe function
- _wexeclpe function
- _execlpe function
- execlpe function
ms.assetid: 07b861da-3e7e-4f1d-bb80-ad69b55e5162
caps.latest.revision: 21
author: corob-msft
ms.author: corob
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 3f91eafaf3b5d5c1b8f96b010206d699f666e224
ms.openlocfilehash: b65df7d6c7276d72682b828e54ee1762ebcebfc1
ms.contentlocale: ja-jp
ms.lasthandoff: 04/01/2017

---
# <a name="execlpe-wexeclpe"></a>_execlpe、_wexeclpe
新しい子プロセスを読み込んで実行します。  
  
> [!IMPORTANT]
>  この API は、Windows ランタイムで実行するアプリケーションでは使用できません。 詳しくは、「 [/ZW でサポートされない CRT 関数](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx)」をご覧ください。  
  
## <a name="syntax"></a>構文  
  
```  
intptr_t _execlpe(   
   const char *cmdname,  
   const char *arg0,  
   ... const char *argn,  
   NULL,  
   const char *const *envp   
);  
intptr_t _wexeclpe(   
   const wchar_t *cmdname,  
   const wchar_t *arg0,  
   ... const wchar_t *argn,  
   NULL,  
   const wchar_t *const *envp   
);  
```  
  
#### <a name="parameters"></a>パラメーター  
 `cmdname`  
 実行するファイルのパス。  
  
 `arg0, ... argn`  
 パラメーターへのポインターのリスト。  
  
 `envp`  
 環境設定へのポインターの配列。  
  
## <a name="return-value"></a>戻り値  
 成功した場合、これらの関数が呼び出しプロセスに戻ることはありません。 戻り値-1 がいる場合、エラーを示す、`errno`グローバル変数を設定します。  
  
|`errno` の値|説明|  
|-------------------|-----------------|  
|`E2BIG`|引数と環境設定には、32 KB を超える領域が必要です。|  
|`EACCES`|指定されたファイルでロック違反または共有違反が発生しています。|  
|`EINVAL`|無効なパラメーター。|  
|`EMFILE`|開いているファイルの数が多すぎます (指定されたファイルは、実行可能ファイルであるかどうかを確認するために開く必要があります)。|  
|`ENOENT`|ファイルまたはパスが見つかりません。|  
|`ENOEXEC`|指定されたファイルが実行可能ファイルでないか、無効な実行可能ファイル形式です。|  
|`ENOMEM`|新しいプロセスを実行するのに十分なメモリがないか、使用できるメモリが破損しているか、または無効なブロックが存在します (呼び出しプロセスが正しく割り当てられていないことを示します)。|  
  
 リターン コードの詳細については、「[_doserrno、errno、_sys_errlist、および _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)」を参照してください。  
  
## <a name="remarks"></a>コメント  
 これらの関数は、新しいプロセスを読み込んで実行し、各コマンド ライン引数を個別のパラメーターとして渡し、環境設定へのポインターの配列も渡します。 これらの関数は、`PATH` 環境変数を使用して、実行するファイルを検索します。  
  
 `_execlpe` 関数は、パラメーターを検証します。 `cmdname` または `arg0` のいずれかが null ポインターであるか、または空の文字列である場合、「[パラメーターの検証](../../c-runtime-library/parameter-validation.md)」に説明されているように、これらの関数は無効なパラメーター ハンドラーを呼び出します。 実行の継続が許可された場合、これらの関数は `errno` を `EINVAL` に設定し、-1 を返します。 新しいプロセスは開始されません。  
  
## <a name="requirements"></a>要件  
  
|関数|必須ヘッダー|オプション ヘッダー|  
|--------------|---------------------|---------------------|  
|`_execlpe`|\<process.h>|\<errno.h>|  
|`_wexeclpe`|\<process.h> または \<wchar.h>|\<errno.h>|  
  
 互換性について詳しくは、「[互換性](../../c-runtime-library/compatibility.md)」を参照してください。  
  
## <a name="example"></a>例  
 「[_exec 関数、_wexec 関数](../../c-runtime-library/exec-wexec-functions.md)」の例を参照してください。  
  
## <a name="see-also"></a>関連項目  
 [プロセス制御と環境制御](../../c-runtime-library/process-and-environment-control.md)   
 [_exec 関数、_wexec 関数](../../c-runtime-library/exec-wexec-functions.md)   
 [abort](../../c-runtime-library/reference/abort.md)   
 [atexit](../../c-runtime-library/reference/atexit.md)   
 [exit、_Exit、_exit](../../c-runtime-library/reference/exit-exit-exit.md)   
 [_onexit、_onexit_m](../../c-runtime-library/reference/onexit-onexit-m.md)   
 [_spawn関数、_wspawn 関数](../../c-runtime-library/spawn-wspawn-functions.md)   
 [system、_wsystem](../../c-runtime-library/reference/system-wsystem.md)