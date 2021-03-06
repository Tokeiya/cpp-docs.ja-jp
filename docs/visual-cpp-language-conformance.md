---
title: "Visual C++ 言語への準拠 | Microsoft Docs"
ms.custom: 
ms.date: 3/1/2017
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-language
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
ms.assetid: 475da6e9-0d78-4b4e-bd23-f41c406c4efe
caps.latest.revision: 11
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
ms.translationtype: HT
ms.sourcegitcommit: 76cd1737728b60a720c0aa8bbc5218ecb66416f2
ms.openlocfilehash: 7f5bb05bf5912dafa99877ed7c9ff6bc4393b28f
ms.contentlocale: ja-jp
ms.lasthandoff: 08/14/2017

---
# <a name="visual-c-language-conformance"></a>Visual C++ 言語への準拠 
このトピックでは、Visual Studio 2017 およびそれ以前のバージョンにおいて、Visual C++ 向けのコンパイラ機能と標準ライブラリ機能が ISO C++03、C++11、C++14、C++17 とドラフト C++20 の言語標準にどの程度準拠しているかをまとめています。 コンパイラと標準ライブラリの各機能の名前には、機能を説明する ISO C++ 標準提案書のリンクが埋め込まれています (ただし、発行時点で提案書が利用できるものに限ります)。 "サポート状況" 列には、機能のサポートが初めて搭載された Visual Studio のバージョンが記載されています。  
  
Visual Studio 2017 で加えられた準拠の強化とその他の変更点の詳細については、「[Visual Studio 2017 の C++ 準拠の強化](cpp-conformance-improvements-2017.md)」と「[Visual Studio 2017 の Visual C++ の新機能](what-s-new-for-visual-cpp-in-visual-studio.md)」をご覧ください。 以前のバージョンにおける準拠の変更点については、[Visual C++ の変更履歴](porting/visual-cpp-change-history-2003-2015.md)に関するページと「[Visual C++ 2003 ～ 2015 の新機能](porting/visual-cpp-what-s-new-2003-through-2015.md)」をご覧ください。 C++ チームからの最新情報は、[Visual C++ チーム ブログ](https://blogs.msdn.microsoft.com/vcblog/)でご覧いただけます。  

 > [!NOTE]
 > Visual Studio 2015 と Visual Studio 2017 では、バイナリに関して重大な変更はありません。
  
## <a name="compiler-features"></a>コンパイラ機能  
  
|機能分野| |  
|----|---|  
|__C++03/11 コア言語機能__|__サポート状況__|
|&nbsp;&nbsp;その他すべて|VS 2015 <sup>[A](#note_A)</sup>|
|&nbsp;&nbsp;名前の 2 段階参照|部分的 <sup>[B](#note_B)</sup>|
|&nbsp;&nbsp;[N2634 式 SFINAE](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2008/n2634.html)|部分的 <sup>[C](#note_C)</sup>|
|&nbsp;&nbsp;[N1653 C99 プリプロセッサ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2004/n1653.htm)|部分的 <sup>[D](#note_D)</sup>|
|&nbsp;&nbsp;[N1988 長整数型](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2006/n1988.pdf)|N/A <sup>[E](#note_E)</sup>|
|__C++14 コア言語機能__|__サポート状況__|
|&nbsp;&nbsp;[N3323 コンテキスト変換での不自然な言い回し](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3323.pdf)|VS 2013|
|&nbsp;&nbsp;[N3472 バイナリ リテラル](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3472.pdf)|VS 2015|
|&nbsp;&nbsp;[N3638 auto と decltype(auto) 戻り値型](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3638.html)|VS 2015|
|&nbsp;&nbsp;[N3648 init キャプチャ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3648.html)|VS 2015|
|&nbsp;&nbsp;[N3649 汎用ラムダ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3649.html)|VS 2015|
|&nbsp;&nbsp;[N3760 [[非推奨]] 属性](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3760.html)|VS 2015|
|&nbsp;&nbsp;[N3778 サイズ割り当て解除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3778.html)|VS 2015|
|&nbsp;&nbsp;[N3781 桁区切り文字](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3781.pdf)|VS 2015|
|&nbsp;&nbsp;[N3651 変数テンプレート](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3651.pdf)|VS 2015.2|
|&nbsp;&nbsp;[N3652 拡張された constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3652.html)|VS 2017|
|&nbsp;&nbsp;[N3653 集計のための NSDMI](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3653.html)|VS 2017|
|&nbsp;&nbsp;[N3664 割り当ての回避/融合](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3664.html)|N/A <sup>[F](#note_F)</sup>|
|__C++17 コア言語機能__|__サポート状況__|
|&nbsp;&nbsp;[N4086 トライグラフの削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4086.html)|VS 2010 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N3922 かっこ付き初期化リストを持つ auto の新しい規則](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3922.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4051 テンプレートのテンプレート パラメーターの typename](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4051.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4266 名前空間と列挙子の属性](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4266.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4267 u8 文字リテラル](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4267.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4230 入れ子になった名前空間の定義](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4230.html)|VS 2015.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N3928 簡潔な static_assert](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3928.pdf)|VS 2017 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0184R0 範囲ベースの for-loop (汎用)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0184r0.html)|VS 2017 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0188R1 [[fallthrough]] 属性](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0188r1.pdf)|VS 2017 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0001R1 register キーワードを削除する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0001r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0002R1 ブール型の operator++ を削除する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0002r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0018R3 値別に *this をキャプチャする](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0018r3.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0028R4 繰り返しのない属性名前空間を使用する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0028r4.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0061R1 __has_include](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0061r1.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0138R2 整数の固定列挙型の direct-list-init](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0138r2.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0170R1 constexpr ラムダ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0170r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0189R1 [[nodiscard]] 属性](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0189r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0212R1 [[maybe_unused]] 属性](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0212r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0217R3 構造化バインド](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0217r3.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0292R2 constexpr if-statements](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0292r2.html)|VS 2017 15.3 <sup>[G](#note_G)</sup>|
|&nbsp;&nbsp;[P0305R1 初期化子のある選択ステートメント](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0305r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0245R1 Hexfloat リテラル](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0245r1.html)|いいえ|
|&nbsp;&nbsp;[N4261 限定変換の修正](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4261.html)|いいえ|
|&nbsp;&nbsp;[N4268 より多くの非型テンプレート引数の許可](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4268.html)|いいえ|
|&nbsp;&nbsp;[N4295 フォールド式](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4295.html)|いいえ|
|&nbsp;&nbsp;[P0003R5 dynamic-exception-specifications の削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0003r5.html)|いいえ|
|&nbsp;&nbsp;[P0012R1 noexcept を型システムに追加する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0012r1.html)|いいえ|
|&nbsp;&nbsp;[P0017R1 集約の初期化 (拡張)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0017r1.html)|いいえ|
|&nbsp;&nbsp;[P0035R4 オーバーアラインの動的メモリ割り当て](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0035r4.html)|いいえ|
|&nbsp;&nbsp;[P0036R0 空の単項 fold をいくつか削除する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0036r0.pdf)|いいえ|
|&nbsp;&nbsp;[P0091R3 クラス テンプレートのテンプレート引数の推論](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0091r3.html)<br />&nbsp;&nbsp;[P0512R0 クラス テンプレートの引数の推論の問題](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0512r0.pdf)|いいえ|
|&nbsp;&nbsp;[P0127R2 auto による非型テンプレート パラメーターの宣言](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0127r2.html)|いいえ|
|&nbsp;&nbsp;[P0135R1 コピー省略の保証](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0135r1.html)|いいえ <sup>[H](#note_H)</sup>|
|&nbsp;&nbsp;[P0136R1 コンストラクター継承の言葉の言い換え](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0136r1.html)|いいえ|
|&nbsp;&nbsp;[P0145R3 式の評価順序の調整](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0145r3.pdf)<br />&nbsp;&nbsp;[P0400R0 関数の引数の評価順序](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0400r0.html)|いいえ|
|&nbsp;&nbsp;[P0195R2 using-declarations のパック拡張](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0195r2.html)|いいえ|
|&nbsp;&nbsp;[P0283R2 識別できない属性を無視する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0283r2.html)|いいえ|
|&nbsp;&nbsp;[P0386R2 インライン変数](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0386r2.pdf)|いいえ|
|&nbsp;&nbsp;[P0522R0 テンプレートのパラメーターと互換性のある引数を照合する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0522r0.html)|いいえ|
|&nbsp;&nbsp;[P0702R1 初期化子リスト ctors のクラス テンプレート引数の推論の修正](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0702r1.html)|いいえ|
|__C++20 Core 言語機能__|__サポート状況__|
|&nbsp;&nbsp;[P0306R4 コンマ省略とコンマ削除のための \_\_VA_OPT\_\_ の追加](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0306r4.pdf)|いいえ|
|&nbsp;&nbsp;[P0329R4 指定の初期化](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0329r4.pdf)|いいえ|
|&nbsp;&nbsp;[P0409R2 ラムダ キャプチャ [=, this] の許可](http://open-std.org/JTC1/SC22/WG21/docs/papers/2017/p0409r2.html)|いいえ|
|&nbsp;&nbsp;[P0428R2 汎用ラムダの使い慣れたテンプレート構文](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0428r2.pdf)|いいえ|
|&nbsp;&nbsp;[P0683R1 ビット フィールドの既定のメンバー初期化子](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0683r1.html)|いいえ|
|&nbsp;&nbsp;[P0704R1 メンバーへの const lvalue ref-qualified ポインターの修正](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0704r1.html)|いいえ|
|&nbsp;&nbsp;[P0734R0 概念](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0734r0.pdf)|いいえ|


## <a name="standard-library-features"></a>標準ライブラリの機能

|機能分野| |
|---|---|
|__C++20 標準ライブラリの機能__|__サポート状況__|
|&nbsp;&nbsp;[P0463R1 エンディアン](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0463r1.html)|いいえ|
|&nbsp;&nbsp;[P0674R1 配列の make_shared()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0674r1.html)|いいえ|
|__C++17 標準ライブラリの機能__|__サポート状況__|
|&nbsp;&nbsp;[P0433R2 標準ライブラリへの、クラス テンプレートのテンプレートの推論の統合](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0433r2.html)<br />&nbsp;&nbsp;[P0739R0 標準ライブラリへのクラス テンプレート引数の推論の統合の強化](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0739r0.html)|いいえ|
|&nbsp;&nbsp;[P0607R0 標準ライブラリのインライン変数](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0607r0.html)|いいえ|
|&nbsp;&nbsp;[P0426R1 char_traits の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0426r1.html)|いいえ|
|&nbsp;&nbsp;[P0030R1 hypot(x, y, z)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0030r1.pdf)|いいえ|
|&nbsp;&nbsp;[P0033R1 enable_shared_from_this の言葉の言い換え](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0033r1.html)|いいえ|
|&nbsp;&nbsp;[P0220R1 ライブラリ基礎 V1](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0220r1.html)|部分的 <sup>[J](#note_J)</sup>|
|&nbsp;&nbsp;[P0414R2 shared_ptr\<T[]>, shared_ptr\<T[N]>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0414r2.html)<br />&nbsp;&nbsp;[P0497R0 配列の shared_ptr の修正](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0497r0.html)|いいえ|
|&nbsp;&nbsp;[P0083R3 マップと設定のスプライス](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0083r3.pdf)<br />&nbsp;&nbsp;[P0508R0 insert_return_type の明確化](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0508r0.html)|いいえ|
|&nbsp;&nbsp;[P0005R4 not_fn()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0005r4.html)<br />&nbsp;&nbsp;[P0358R1 not_fn() の修正](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0358r1.html)|いいえ|
|&nbsp;&nbsp;[P0067R5 基本文字列変換](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0067r5.html)|いいえ|
|&nbsp;&nbsp;[P0618R0 \<codecvt> を非推奨にする](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0618r0.html)|いいえ|
|&nbsp;&nbsp;[P0521R0 shared_ptr::unique() の廃止](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0521r0.html)|いいえ|
|&nbsp;&nbsp;[P0174R2 残留ライブラリ パーツの廃止](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0174r2.html)|いいえ|
|&nbsp;&nbsp;[P0003R5 動的例外指定の削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0003r5.html)|いいえ|
|&nbsp;&nbsp;[P0302R1 std::function のアロケーター サポートの削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0302r1.html)|いいえ|
|&nbsp;&nbsp;[N4562 Library Fundamentals: \<memory_resource>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#memory.resource.synop)<br />&nbsp;&nbsp;[P0337R0 polymorphic_allocator 割り当ての削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0337r0.html)|いいえ|
|&nbsp;&nbsp;[P0024R2 並列アルゴリズム](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0024r2.html)<br />&nbsp;&nbsp;[P0336R1 並列実行ポリシーの名前変更](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0336r1.pdf)<br />&nbsp;&nbsp;[P0394R4 並列アルゴリズムの例外処理の terminate()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0394r4.html)<br />&nbsp;&nbsp;[P0452R1 \<numeric> 並列アルゴリズムの統合](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0452r1.html)|いいえ|
|&nbsp;&nbsp;[P0226R1 数学的特殊関数](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0226r1.pdf)|いいえ|
|&nbsp;&nbsp;[P0218R1 \<filesystem>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0218r1.html)<br />&nbsp;&nbsp;[P0219R1 ファイル システムの相対パス](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0219r1.html)<br />&nbsp;&nbsp;[P0317R1 ファイル システムのディレクトリ エントリのキャッシュ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p03179r1.html)<br />&nbsp;&nbsp;[P0392R0 ファイル システム パスの string_view のサポート](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0392r0.pdf)<br />&nbsp;&nbsp;[P0430R2 POSIX 以外のファイル システムのサポート](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0430r2.pdf)<br />&nbsp;&nbsp;[P0492R2 ファイル システムに関する NB コメントの解決](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0492r2.html)|いいえ <sup>[K](#note_K)</sup>|
|&nbsp;&nbsp;[N4562 Library Fundamentals: ボイヤー-ムーア法による search()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#func.searchers.boyer_moore)<br/>&nbsp;&nbsp;[P0253R1 サーチャーの戻り値の型を修正する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0253r1.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0031R0 \<array> (再度) と \<iterator> の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0031r0.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0040R3 メモリ管理ツールの拡張](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0040r3.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0084R2 戻り値の型の配置](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0084r2.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0152R1 atomic::is_always_lock_free](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0152r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0154R1 hardware_destructive_interference_size など](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0154r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0156R2 可変個引数 lock\_guard の名前を scoped\_lock に変更](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0156r2.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0258R2 has_unique_object_representations](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0258r2.html)|VS 2017 15.3 <sup>[L](#note_L)</sup>|
|&nbsp;&nbsp;[P0295R0 gcd()、lcm()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0295r0.pdf)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0298R3 std::byte](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0298r3.pdf)|VS 2017 15.3 <sup>[17](#note_17)[byte](#note_byte)</sup>|
|&nbsp;&nbsp;[P0403R1 \<string_view> の UDL ("meow"sv など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0403r1.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0418R2 アトミック compare_exchange memory_order 要件](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0418r2.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0435R1 common_type の総点検](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0435r1.pdf)<br />&nbsp;&nbsp;[P0548R1 common\_type と期間の調整](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0548r1.pdf)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0505R0 \<chrono> の constexpr (再度)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0505r0.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[P0513R0 ハッシュの汚染](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0513r0.pdf)<br />&nbsp;&nbsp;[P0599R1 noexcept ハッシュ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0599r1.pdf)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0516R0 shared_future コピーを noexcept としてマークする](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0516r0.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0517R0 future_errc から future_error を構築する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0517r0.html)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0558R1 atomic <T> 名前付き基底クラスの不一致の解消](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0558r1.pdf)|VS 2017 15.3 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0604R0 is\_callable/result\_of を invoke\_result、is\_invocable、is\_nothrow\_invocable に変更](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2017/p0604r0.html)|VS 2017 15.3 <sup>[17](#note_17)</sup>|
|&nbsp;&nbsp;[N4562 Library Fundamentals: \<algorithm> sample()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#alg.random.sample)|VS 2017|
|&nbsp;&nbsp;[N4562 Library Fundamentals: \<any>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#any)|VS 2017|
|&nbsp;&nbsp;[N4562 Library Fundamentals: \<optional>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#optional)|VS 2017|
|&nbsp;&nbsp;[N4562 Library Fundamentals: \<string_view>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#string.view)|VS 2017|
|&nbsp;&nbsp;[N4562 Library Fundamentals: \<tuple> apply()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4562.html#tuple)|VS 2017|
|&nbsp;&nbsp;[P0032R3 variant/any/optional の同種インターフェイス](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0032r3.pdf)|VS 2017|
|&nbsp;&nbsp;[P0077R2 is_callable、is_nothrow_callable](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0077r2.html)|VS 2017|
|&nbsp;&nbsp;[P0088R3 \<variant>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0088r3.html)|VS 2017|
|&nbsp;&nbsp;[P0163R0 shared_ptr::weak_type](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0163r0.html)|VS 2017|
|&nbsp;&nbsp;[P0209R2 make_from_tuple()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0209r2.pdf)|VS 2017|
|&nbsp;&nbsp;[P0254R2 string_view と std::string の統合](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0254r2.pdf)|VS 2017|
|&nbsp;&nbsp;[P0307R2 Optional の同等以上 (再度)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0307r2.pdf)|VS 2017|
|&nbsp;&nbsp;[P0393R3 バリアントの同等以上](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0393r3.html)|VS 2017|
|&nbsp;&nbsp;[P0504R0 in_place_t/in_place_type_t\<T>/in_place_index_t\<I> 再考](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0504r0.html)|VS 2017|
|&nbsp;&nbsp;[P0510R0 Nothing、Arrays、References、Incomplete Types のバリアントを拒否する](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0510r0.html)|VS 2017|
|&nbsp;&nbsp;[P0025R1 clamp()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0025r1.html)|VS 2015.3|
|&nbsp;&nbsp;[P0185R1 is_swappable、is_nothrow_swappable](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0185r1.html)|VS 2015.3|
|&nbsp;&nbsp;[P0272R1 Non-const basic_string::data()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0272r1.html)|VS 2015.3|
|&nbsp;&nbsp;[N4387 ペアとタプルの改善](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4387.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4508 shared_mutex (時間測定なし)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4508.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0004R1 使用されていない Iostreams エイリアスの削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0004r1.html)|VS 2015.2 <sup>[rem](#note_rem)</sup>|
|&nbsp;&nbsp;[P0006R0 型の特徴の変数テンプレート (is_same_v など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0006r0.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0007R1 as_const()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0007r1.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0013R1 論理演算子の型の特徴 (conjunction など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0013r1.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0074R0 owner_less\<>](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0074r0.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0092R1 \<chrono> floor()、ceil()、round()、abs()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0092r1.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0156R0 可変個引数 lock_guard](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/p0156r0.html)|VS 2015.2 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N3911 void_t](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3911.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4089 unique_ptr\<T[]> の安全な変換](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4089.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4169 invoke()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4169.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4190 auto_ptr、random_shuffle()、および古い \<functional> Stuff の削除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4190.htm)|VS 2015 <sup>[rem](#note_rem)</sup>|
|&nbsp;&nbsp;[N4258 noexcept クリーンアップ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4258.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4259 uncaught_exceptions()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4259.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4277 普通にコピー可能 reference_wrapper](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4277.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4279 map/unordered_map の insert_or_assign()/try_emplace()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4279.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4280 size()、empty()、data()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n4280.pdf)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4366 unique_ptr 割り当ての正確な制約](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4366.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4389 bool_constant](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4389.html)|VS 2015 <sup>[14](#note_14)</sup>|
|&nbsp;&nbsp;[P0063R3 C11 標準ライブラリ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2016/p0063r3.html)|VS 2015 <sup>[C11](#note_C11)[14](#note_14)</sup>|
|&nbsp;&nbsp;[N4510 vector/list/forward_list の不完全な型のサポート](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2015/n4510.html)|VS 2013 <sup>[14](#note_14)</sup>|
|__C++14 標準ライブラリの機能__|__サポート状況__|
|&nbsp;&nbsp;[N3462 SFINAE 対応 result_of](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3462.html)|VS 2015.2|
|&nbsp;&nbsp;[N3302 \<complex> の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2011/n3302.html)|VS 2015|
|&nbsp;&nbsp;[N3469 \<chrono> の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3469.html)|VS 2015|
|&nbsp;&nbsp;[N3470 \<array> の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3470.html)|VS 2015|
|&nbsp;&nbsp;[N3471 \<initializer_list>、\<tuple>、\<utility> の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3471.html)|VS 2015|
|&nbsp;&nbsp;[N3545 integral_constant::operator()()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3545.pdf)|VS 2015|
|&nbsp;&nbsp;[N3642 \<chrono>、\<string> の UDL (1729ms、"meow"s など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3642.pdf)|VS 2015|
|&nbsp;&nbsp;[N3644 Null 前進反復子](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3644.pdf)|VS 2015|
|&nbsp;&nbsp;[N3654 quoted()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3654.html)|VS 2015|
|&nbsp;&nbsp;[N3657 異種連想ルックアップ](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3657.htm)|VS 2015|
|&nbsp;&nbsp;[N3658 integer_sequence](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3658.html)|VS 2015|
|&nbsp;&nbsp;[N3659 shared_mutex (時間計測あり)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3659.html)|VS 2015|
|&nbsp;&nbsp;[N3668 exchange()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3668.html)|VS 2015|
|&nbsp;&nbsp;[N3669 const のない constexpr メンバー関数の修正](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3669.pdf)|VS 2015|
|&nbsp;&nbsp;[N3670 get\<T>()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3670.html)|VS 2015|
|&nbsp;&nbsp;[N3671 デュアルレンジ equal()、is_permutation()、mismatch()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3671.html)|VS 2015|
|&nbsp;&nbsp;[N3778 サイズ割り当て解除](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3778.html)|VS 2015|
|&nbsp;&nbsp;[N3779 \<complex> の UDL (3.14i など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3779.pdf)|VS 2015|
|&nbsp;&nbsp;[N3789 \<functional> の constexpr](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3789.htm)|VS 2015|
|&nbsp;&nbsp;[N3887 tuple_element_t](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3887.pdf)|VS 2015|
|&nbsp;&nbsp;[N3891 shared_mutex (時間指定あり) の名前を shared_timed_mutex に変更](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3891.htm)|VS 2015|
|&nbsp;&nbsp;[N3346 コンテナー要素の最小要件](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3346.pdf)|VS 2013|
|&nbsp;&nbsp;[N3421 透過的な演算子のファンクター (less\<> など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2012/n3421.htm)|VS 2013|
|&nbsp;&nbsp;[N3655 \<type_traits> のエイリアス テンプレート (decay_t など)](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3655.pdf)|VS 2013|
|&nbsp;&nbsp;[N3656 make_unique()](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2013/n3656.htm)|VS 2013|
|&nbsp;&nbsp;[N3924 rand() を推奨しない](http://www.open-std.org/jtc1/sc22/wg21/docs/papers/2014/n3924.pdf)|N/A|  
  
複数の提案書がまとめて記載されている箇所は、ある機能が報告されて標準になり、その後、その機能を強化または拡張するための提案書が 1 つ以上報告されたことを示しています。 これらの機能はまとめて実装されます。  
  
### <a name="supported-values"></a>サポート状況の値  
__いいえ__は、未実装という意味です。  
__一部__は、Visual Studio 2017 への実装が一部のみであるという意味です。 詳細については、「ノート」セクションを参照してください。  
__該当なし__は、提案書で機能が説明されていないことを意味しています。 これらのペーパーでは、標準の言語が変更されています。ただし、実装者のいかなる作品も作成されていません。 ここに記載するのは、完全性を期すためです。  
__VS 2010__ は、Visual Studio 2010 でサポートされている機能を示しています。  
__VS 2013__ は、Visual Studio 2013 でサポートされている機能を示しています。  
__VS 2015__ は、Visual Studio 2015 RTM でサポートされている機能を示します。  
__VS 2015.2__ と __VS 2015.3__ はそれぞれ、Visual Studio 2015 更新プログラム 2 と Visual Studio 2015 更新プログラム 3 でサポートされている機能を示します。  
__VS 2017__ は、Visual Studio 2017 RTM でサポートされている機能を示します。  
__VS 2017 15.3__ は、Visual Studio 2017 バージョン 15.3 でサポートされている機能を示します。  
  
### <a name="notes"></a>メモ  
<a name="note_A"></a>__A__ これにより、C++11 で使用されていない、C++03 の動的例外指定が無視されます。 この指定を実装する予定はありません。将来の C++ 標準から削除される予定です。  
<a name="note_B"></a>__B__ 2 フェーズの名前参照のコンパイラのサポートは改良されましたが、まだ完成はしていません。  
<a name="note_C"></a>__C__ Visual Studio 2015 更新プログラム 2 以降、SFINAE 式がコンパイラでサポートされています。標準ライブラリにはそれで十分でしたが、サポートは不完全なままです。  
<a name="note_D"></a>__D__ Visual Studio 2017 では、C99 プリプロセッサ ルールはコンパイラで完全にサポートされていません。 可変個引数マクロがサポートされますが、プリプロセッサの動作にたくさんのバグがあります。  
<a name="note_E"></a>__E__これは該当なしとしてマークされています。拡張整数型のサポートがコンパイラに許可されていますが、必須ではないためです。  GCC や Clang と同様に、サポートしないことを選択しました。  
<a name="note_F"></a>__F__ 同様に、これは該当なしとしてマークされています。この最適化の実装がコンパイラに許可されていますが、必須ではないためです。  
<a name="note_G"></a>__G__ [/std:c++14](./build/reference/std-specify-language-standard-version.md) で、非表示にできる警告でサポートされています。  
<a name="note_H"></a>__H__ この機能は Visual Studio 2017 バージョン 15.3 より前のバージョンで提供されていましたが、バグが見つかったため、リリースから削除されました。  
<a name="note_J"></a>__J__ Visual Studio 2015 では完全ではなかった機能は、この表の他の箇所に記載されています。  
<a name="note_K"></a>__K__ ファイル システム TS は歴史的な理由から \<experimental/filesystem> と \<filesystem> の両方で実装されていますが、名前空間が移動される前に実装を修正する必要があります。 これが完了するまで、機能は未実装としてマークされます。  
<a name="note_L"></a>__L__ コンパイラ組み込みでサポートされています。 この組み込みは Clang ではまだ使用できません。 この機能は使用できますが、Intellisense ではまだ有効ではありません。   
<a name="note_14"></a>__14__ これらの C++17 機能は、[/std:c++14](./build/reference/std-specify-language-standard-version.md) (既定) が指定されているときでも、常に有効です。 この理由は、**/std** オプションを導入する前に機能が実装されたため、または条件付きの実装が許容範囲を超えて複雑なためです。  
<a name="note_17"></a>__17__ これらの機能は [/std:c++17](./build/reference/std-specify-language-standard-version.md) (または [/std:c++latest](./build/reference/std-specify-language-standard-version.md)) コンパイラ オプションにより保護されています。  
<a name="note_byte"></a>__byte__ `std::byte` は [/std:c++17](./build/reference/std-specify-language-standard-version.md) (または [/std:c++latest](./build/reference/std-specify-language-standard-version.md)) により有効になっていますが、Windows SDK のヘッダーと競合することがあるため、細かいオプトアウト マクロがあります。 `_HAS_STD_BYTE` を `0` として定義することで無効にできます。  
<a name="note_C11"></a>__C11__ ユニバーサル CRT では、C++17 で必要となる C11 標準ライブラリの部分を実装しました。C99 `strftime()` E/O 代替変換指定子、C11 `fopen()` 排他モード、C11 `aligned_alloc()` は除きます。 C11 は `aligned_alloc()` を、Microsoft の `free()` の実装と互換性のない方法で指定した、つまり、その `free()` は高度に割り当てられたアロケーションを処理できなければならないため、後者が実装される可能性は低いです。  
<a name="note_rem"></a>__rem__ 機能が [/std:c++17](./build/reference/std-specify-language-standard-version.md) (または [/std:c++latest](./build/reference/std-specify-language-standard-version.md)) コンパイラ オプションが指定されたときに削除されます。 これらの機能には、`_HAS_AUTO_PTR_ETC`、`_HAS_FUNCTION_ALLOCATOR_SUPPORT`、`_HAS_OLD_IOSTREAMS_MEMBERS`、`_HAS_UNEXPECTED` のオプトアウト マクロがあります。
  
## <a name="see-also"></a>関連項目  
[C++ 言語リファレンス](cpp/cpp-language-reference.md)  
[C++ 標準ライブラリ](standard-library/cpp-standard-library-reference.md)   
[Visual Studio 2017 での C++ 準拠の改善](cpp-conformance-improvements-2017.md)  
[Visual Studio 2017 の Visual C++ の新機能](what-s-new-for-visual-cpp-in-visual-studio.md)  
[Visual C++ 2003 ～ 2015 の変更履歴](porting/visual-cpp-change-history-2003-2015.md)  
[2003 から 2015 の Visual C++ の新機能](porting/visual-cpp-what-s-new-2003-through-2015.md)  
[Visual C++ チーム ブログ](https://blogs.msdn.microsoft.com/vcblog/)  

