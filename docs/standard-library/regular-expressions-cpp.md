---
title: "正規表現 (C++) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- Visual C++, regular expressions
- regular expressions, Visual C++
- regular expressions
ms.assetid: aafe202a-1d96-4b36-a270-d676dfd3c51c
caps.latest.revision: 12
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
ms.sourcegitcommit: 4bac7b2942f9d72674b8092dc7bf64174dd3c349
ms.openlocfilehash: ac4dc70360682aff3a28eabeed0e4f05e4c509a8
ms.contentlocale: ja-jp
ms.lasthandoff: 04/24/2017

---
# <a name="regular-expressions-c"></a>正規表現 (C++)
C++ 標準ライブラリでは、複数の正規表現の文法をサポートします。 正規表現を使用する場合は、使用可能な文法バリエーションを説明します。  
  
##  <a name="regexgrammar"></a> 正規表現の文法  
使用する正規表現の文法がで指定のいずれかを使用して、`std::regex_constants::syntax_option_type`列挙値。 Std::regex_constants では、これらの正規表現の文法が定義されています。

-   `ECMAScript`: これは、JavaScript と .NET 言語で使用される文法に最も近いです。
-   `basic`: POSIX の基本的な正規表現または BRE です。
-   `extended`: POSIX では、正規表現または ERE を拡張します。
-   `awk`: これは`extended`、が、非印刷文字のエスケープを追加します。
-   `grep`: これは`basic`、はも許可されている改行文字 ('\n') の代替を区切る文字です。
-   `egrep`: これは`extended`、改行文字 alternatios を分離することもできますが、します。

既定では、文法が指定されていない場合`ECMAScript`と見なされます。 1 つだけの文法を指定することがあります。  
  
文法、に加えていくつかのフラグを適用できます。  
-   `icase`: 一致する場合に、大文字小文字を区別します。  
-   `nosubs`: 無視マークされた一致する (つまり、かっこで囲んだ式) です。代替文字列は格納されません。  
-   `optimize`: 大きい構築時の可能な経費と高速で一致するようにします。  
-   `collate`: ロケール依存型の照合順序 (たとえば、フォーム"[a ~ z]"の範囲) を使用します。  
  
0 個以上のフラグは、正規表現エンジンの動作を指定する文法と組み合わせることがあります。 だけをフラグを指定すると、`ECMAScript`文法と見なされます。

### <a name="element"></a>要素  
 要素は次のいずれかです。  
  
-   ターゲット シーケンスの同じ文字と一致する*通常の文字*。  
  
-   ターゲット シーケンスの改行を除く任意の文字と一致する*ワイルドカード文字*。  
  
-   *角かっこ表現*。"[`expr`]" の形式の場合は、ターゲット シーケンス内で、正規表現 `expr` で定義されるセットにある文字または照合要素と一致します。"[^`expr`]" の形式の場合は、ターゲット シーケンス内で、正規表現 `expr` で定義されるセットにはない文字または照合要素と一致します。  
  
     正規表現 `expr` には、次の任意の組み合わせを含めることができます。  
  
    -   個々の文字。 その文字を、`expr` で定義されたセットに追加します。  
  
    -   "`ch1`-`ch2`" の形式の*文字範囲*。 閉じた範囲 [`ch1`, `ch2`] の値で表される文字を、`expr` で定義されたセットに追加します。  
  
    -   "[:`name`:]" の形式の*文字クラス*。 名前付きのクラスの文字を、`expr` で定義されたセットに追加します。  
  
    -   "[=`elt`=]" の形式の*等価クラス*。 `elt` と同じ照合要素を、`expr` で定義されたセットに追加します。  
  
    -   "[.`elt`.]" の形式の*照合シンボル*。 照合要素 `elt` を `expr` で定義されたセットに追加します。  
  
-   *アンカー*。 アンカー "^" はターゲット シーケンスの先頭に一致します。アンカー "$" はターゲット シーケンスの末尾に一致します。  
  
 "( *部分式* )"、または `basic` や `grep` の場合は "\\( *部分式* \\)" の形式の*キャプチャ グループ*。区切り記号で囲まれたパターンと一致するターゲット シーケンス内の文字シーケンスと一致します。  
  
-   "\\`k`" の形式の*単一文字エスケープ*は、ターゲット シーケンス内の文字 `k` と一致します。  
  
 次に例を示します。  
  
-   "a" は、ターゲット シーケンス "a" と一致しますが、ターゲット シーケンス "B"、"b"、または "c" とは一致しません。  
  
-   "." は、すべてのターゲット シーケンス "a"、"B"、"b"、および "c" と一致します。  
  
-   "[b-z]" は、ターゲット シーケンス "b" および "c" と一致しますが、ターゲット シーケンス "a" または "B" とは一致しません。  
  
-   "[:lower:]" は、ターゲット シーケンス "a"、"b"、および "c" と一致しますが、ターゲット シーケンス "B" とは一致しません。  
  
-   "(a)" は、ターゲット シーケンス "a" と一致し、キャプチャ グループ 1 をサブシーケンス "a" に関連付けますが、ターゲット シーケンス "B"、"b"、または "c" とは一致しません。  
  
 `ECMAScript`、`basic`、および `grep` では、要素は、"\\`dd`" の形式で*前方参照*にすることもできます。ここで、`dd` が表す 10 進値 N は、N 番目の*キャプチャ グループ*と一致する文字のシーケンスと同じであるターゲット シーケンス内の文字シーケンスと一致します。 たとえば、"(a)\1" はターゲット シーケンス "aa" と一致します。これは、最初の (唯一の) キャプチャ グループが最初のシーケンス "a" と一致し、\1 が最後のシーケンス "a" と一致するためです。  
  
 `ECMAScript` では、要素として次のいずれかも使用できます。  
  
-   "(: *部分式*)" 形式の*非キャプチャ グループ*。 区切り記号の間のパターンと一致したターゲット シーケンス内の文字のシーケンスと一致します。  
  
-   "\f"、"\n"、"\r"、"\t"、または "\v" の形式の制限付き*ファイル形式エスケープ*。 これらは、ターゲット シーケンスのフォーム フィード、改行、復帰、水平タブ、および垂直タブに、それぞれ一致します。  
  
-   "(= *部分式* )" の形式の*肯定アサート*。 区切り記号の間のパターンと一致するターゲット シーケンス内の文字シーケンスと一致しますが、ターゲット シーケンス内の一致項目の位置を変更しません。  
  
-   A*否定アサート*フォームの"(! *subexpression* )"です。 区切り記号の間のパターンと一致しないターゲット シーケンス内の任意の文字シーケンスと一致し、ターゲット シーケンス内の一致項目の位置を変更しません。  
  
-   "\x`hh`" の形式の *16 進数のエスケープ シーケンス*。 2 個の 16 進数字 `hh` で表されるターゲット シーケンス内の文字と一致します。  
  
-   "\u`hhhh`" の形式の *Unicode エスケープ シーケンス*。 4 個の 16 進数字 `hhhh` で表されるターゲット シーケンス内の文字と一致します。  
  
-   "\c`k`" の形式の*制御エスケープ シーケンス*。 文字 `k` によって指定される制御文字と一致します。  
  
-   "\b" の形式の*単語境界アサート*。 ターゲット シーケンス内の現在位置が*単語境界*の直後にある場合に一致します。  
  
-   "\B" の形式の*否定単語境界アサート*。 ターゲット シーケンス内の現在位置が*単語境界*の直後にない場合に一致します。  
  
-   "\d"、"\D"、"\s"、"\S"、"\w"、"\W" の形式の *dsw 文字エスケープ*。 文字クラスに短い名前を指定します。  
  
 次に例を示します。  
  
-   "(:a)" はターゲット シーケンス "a" と一致しますが、キャプチャ グループ 1 はないため "(:a)\1" は無効です。  
  
-   "(=a)a" はターゲット シーケンス "a" と一致します。 肯定アサートは、ターゲット シーケンス内の最初のシーケンス "a" と一致し、正規表現内の最後の "a" はターゲット シーケンス内の最初のシーケンス "a" と一致します。  
  
-   "(!a)a" はターゲット シーケンス "a" と一致しません。  
  
-   "a \b。" ターゲット シーケンスと一致"、~"、ターゲット シーケンス"ab"は一致しません。  
  
-   "a \b。" ターゲット シーケンス"ab"と一致しますが、ターゲット シーケンスと一致しません"、~"です。  
  
 `awk` では、要素として次のいずれかも使用できます。  
  
-   "\\\\"、"\a"、"\b"、"\f"、"\n"、"\r"、"\t"、または "\v" の形式の*ファイル形式エスケープ*。 これらは、ターゲット シーケンスの円記号、アラート、バックスペース、フォーム フィード、改行、復帰、水平タブ、および垂直タブに、それぞれ一致します。  
  
-   "\\`ooo`" の形式の *8 進数のエスケープ シーケンス*。 1 個、2 個、または 3 個の 8 進数の数字 `ooo` で表される値であるターゲット シーケンスの文字と一致します。  
  
### <a name="repetition"></a>繰り返し  
 *肯定アサート*、*否定アサート*、*アンカー*の要素が繰り返し数を配置できます。 最も一般的な種類の繰り返し数は、"{`min`,`max`}" の形式になります。または、`basic` および `grep` では、"\\{`min`,`max`\\}" の形式になります。 後にこの形式の繰り返し数が続く要素は、要素に一致するシーケンスが少なくとも `min` 回連続して発生し、最大で `max` 回連続して発生する場合に一致します。 たとえば、"a{2,3}" は、ターゲット シーケンス "aa" およびターゲット シーケンス "aaa" と一致しますが、ターゲット シーケンス "a" やターゲット シーケンス "aaaa" とは一致しません。  
  
 繰り返し数は、次のいずれかの形式で指定することもできます。  
  
-   "{`min`}"、または `basic` や `grep` の "\\{`min`\\}"。 これは、"{`min`,`min`}" と同じです。  
  
-   "{`min`,}"、または `basic` や `grep` の "\\{`min`,\\}"。 これは、"{`min`,unbounded}" と同じです。  
  
-   "*". これは、"{0,unbounded}" と同じです。  
  
 次に例を示します。  
  
-   "a{2}" は、ターゲット シーケンス "aa" と一致しますが、ターゲット シーケンス "a" やターゲット シーケンス "aaa" とは一致しません。  
  
-   "a{2,}" は、ターゲット シーケンス "aa"、ターゲット シーケンス "aaa" などと一致しますが、ターゲット シーケンス "a" とは一致しません。  
  
-   "a*" は、ターゲット シーケンス ""、ターゲット シーケンス "a"、ターゲット シーケンス "aa" などと一致します。  
  
 `basic` と `grep` を除くすべての文法では、繰り返し数は次のいずれかの形式で指定することもできます。  
  
-   "". これは、"{0,1}" と同じです。  
  
-   "+". これは、"{1,unbounded}" と同じです。  
  
 次に例を示します。  
  
-   "a" は、ターゲット シーケンス "" および "a" と一致しますが、ターゲット シーケンス "aa" とは一致しません。  
  
-   "a+" は、ターゲット シーケンス "a"、ターゲット シーケンス "aa" などと一致しますが、ターゲット シーケンス "" とは一致しません。  
  
 `ECMAScript` では、繰り返し数のすべての形式で後に文字 " を続けることによって、*繰り返しの最短一致*を指定できます。  
  
### <a name="concatenation"></a>連結  
 正規表現の要素は、*繰り返し数*の有無にかかわらず、長い正規表現を形成するために連結することもできます。 結果の正規表現は、個々の要素と一致したシーケンスの連結であるターゲット シーケンスと一致します。 たとえば、"a{2,3}b" は、ターゲット シーケンス "aab" およびターゲット シーケンス "aaab" と一致しますが、ターゲット シーケンス "ab" やターゲット シーケンス "aaaab" とは一致しません。  
  
### <a name="alternation"></a>代替  
 `basic` と `grep` を除くすべての正規表現の文法では、連結された正規表現の後に文字 "&#124;" と別の連結された正規表現を続けることができます。 連結した正規表現はいくつでもこのように組み合わせることができます。 結果の正規表現は、連結された正規表現のいずれかと一致するターゲット シーケンスと一致します。  
  
 複数の連結された正規表現がターゲット シーケンスと一致する場合、`ECMAScript` では、連結された正規表現のうちで最初にシーケンスと一致したものが一致 (*最初の一致*) として選択されます。他の正規表現文法では*最長一致*となるものが選択されます。 たとえば、"ab&#124;cd" は、ターゲット シーケンス "ab" およびターゲット シーケンス "cd" と一致しますが、ターゲット シーケンス "abd" やターゲット シーケンス "acd" とは一致しません。  
  
 `grep` と `egrep` では、改行文字 ("\n") を使用して代替を区切ることができます。  
  
### <a name="subexpression"></a>部分式  
 `basic` と `grep` では、部分式は連結です。 他の正規表現文法では、部分式は代替です。  
  
##  <a name="grammarsummary"></a> 文法概要  
 次の表に、さまざまな正規表現文法で使用できる機能の概要を示します。  
  
|要素|基本|拡張|ECMAScript|grep|egrep|awk|  
|-------------|---------|---------|----------|----------|-----------|---------|  
|"&#124;" を使用する代替||+|+||+|+|  
|"\n" を使用する代替||||+|+||  
|アンカー|+|+|+|+|+|+|  
|前方参照|+||+|+|||  
|角かっこ表現|+|+|+|+|+|+|  
|"()" を使用するキャプチャ グループ||+|+||+|+|  
|"\\(\\)" を使用するキャプチャ グループ|+|||+|||  
|制御エスケープ シーケンス|||+||||  
|dsw 文字エスケープ|||+||||  
|ファイル形式エスケープ|||+|||+|  
|16 進数のエスケープ シーケンス|||+||||  
|単一文字エスケープ|+|+|+|+|+|+|  
|否定アサート|||+||||  
|否定単語境界アサート|||+||||  
|非キャプチャ グループ|||+||||  
|繰り返しの最短一致|||+||||  
|8 進数のエスケープ シーケンス||||||+|  
|通常文字|+|+|+|+|+|+|  
|肯定アサート|||+||||  
|"{}" を使用する繰り返し||+|+||+|+|  
|"\\{\\}" を使用する繰り返し|+|||+|||  
|"*" を使用する繰り返し|+|+|+|+|+|+|  
|" と "+" を使用する繰り返し||+|+||+|+|  
|unicode エスケープ シーケンス|||+||||  
|ワイルドカード文字|+|+|+|+|+|+|  
|単語境界アサート|||+||||  
  
##  <a name="semanticdetails"></a> セマンティクス詳細  
  
### <a name="anchor"></a>アンカー  
 アンカーは、文字ではなく、ターゲット文字列内の位置と一致します。 "^" はターゲット文字列の先頭に一致します。"$" はターゲット文字列の末尾に一致します。  
  
### <a name="back-reference"></a>前方参照  
 前方参照は、円記号とそれに続く 10 進値 N です。これは N 番目の*キャプチャ グループ* のコンテンツと一致します。 N の値は前方参照の前にあるキャプチャ グループの数を超えないようにする必要があります。 `basic` と `grep` では、N の値は円記号に続く 10 進数字によって決まります。 `ECMAScript` では、N の値は円記号の直後に続くすべての 10 進数字によって決まります。 したがって、`basic` と `grep` では、正規表現に 9 個を超えるキャプチャ グループが存在する場合でも、N の値が 9 を超えることはありません。 `ECMAScript` では、N の値は無制限です。  
  
 次に例を示します。  
  
-   "((a+)(b+))(c+)\3" は、ターゲット シーケンス "aabbbcbbb" と一致します。 前方参照 "\3" は、3 番目のキャプチャ グループのテキスト、つまり "(b+)" と一致します。 これはターゲット シーケンス "aabbbcbb" と一致しません。  
  
-   "(a)\2" は有効ではありません。  
  
-   "(b(((((((((a))))))))))\10" は、`basic` と `ECMAScript` では意味が異なります。 `basic` では、前方参照は "\1" です。 前方参照は最初のキャプチャ グループ (つまり、"(b" で始まり、最後の ")" で終わり、前方参照の前にある) の内容と一致し、最後の "0" は通常文字 "0" と一致します。 `ECMAScript` では、前方参照は "\10" です。 これは、10 番目のキャプチャ グループ、つまり最も内側のものと一致します。  
  
### <a name="bracket-expression"></a>角かっこ表現  
 角かっこ表現は、一連の文字と*照合要素*を定義します。 角かっこ表現が文字 "^" で始まる場合、ターゲット シーケンス内の現在の文字と一致する要素がセットにないときに一致と見なされます。 それ以外の場合、セット内のいずれかの要素がターゲット シーケンスの現在の文字と一致するときに一致と見なされます。  
  
 文字セットは、*個々の文字*、*文字範囲*、*文字クラス*、*等価クラス*、*照合シンボル*の組み合わせを記述することによって定義できます。  
  
### <a name="capture-group"></a>キャプチャ グループ  
 キャプチャ グループは正規表現文法の 1 つの単位として内容をマークし、内容と一致する対象のテキストにラベルを付けます。 各キャプチャ グループに関連付けられるラベルは数値で、現在のキャプチャ グループを示す左かっこを含め、この左かっこまでのキャプチャ グループを示す左かっこの数をカウントすることによって決定されます。 この実装では、キャプチャ グループの最大数は 31 になります。  
  
 次に例を示します。  
  
-   "ab+" は、ターゲット シーケンス "abb" と一致しますが、ターゲット シーケンス "abab" とは一致しません。  
  
-   "(ab)+" は、ターゲット シーケンス "abb" と一致しませんが、ターゲット シーケンス "abab" とは一致します。  
  
-   "((a+)(b+))(c+)" は、ターゲット シーケンス "aabbbc" と一致し、キャプチャ グループ 1 をサブシーケンス "aabbb" に、キャプチャ グループ 2 をサブシーケンス "aa" に、キャプチャ グループ 3 を "bbb" に、キャプチャ グループ 4 をサブシーケンス "c" に関連付けます。  
  
### <a name="character-class"></a>文字クラス  
 角かっこ表現内の文字クラスは、角かっこ表現で定義された文字セットに名前付きクラスのすべての文字を追加します。 文字クラスを作成するには、"[:" の後にクラスの名前、その後に ":]" を使用します。 内部的には、文字クラスの名前は `id = traits.lookup_classname` を呼び出すことで認識されます。 `ch` が true を返す場合、文字はその `traits.isctype(ch, id)` クラスに属しています。 既定の `regex_traits` テンプレートは、次の表のクラス名をサポートします。  
  
|クラス名|説明|  
|----------------|-----------------|  
|"alnum"|小文字、大文字、および数字|  
|"alpha"|小文字および大文字|  
|"blank"|空白またはタブ|  
|"cntrl"|*ファイル形式エスケープ*文字|  
|"digit"|数字|  
|"graph"|小文字、大文字、数字、および句読点|  
|"lower"|小文字|  
|"print"|小文字、大文字、数字、句読点、および空白|  
|"punct"|句読点|  
|"space"|space|  
|"upper|大文字|  
|"xdigit"|数字、"a"、"b"、"c"、"d"、"e"、"f"、"A"、"B"、"C"、"D"、"E"、"F"|  
|"d"|digit と同じ|  
|"s"|space と同じ|  
|"w"|alnum と同じ|  
  
### <a name="character-range"></a>文字範囲  
 角かっこ表現内の文字範囲は、角かっこ表現で定義された文字セットに範囲内のすべての文字を追加します。 文字範囲を作成するには、範囲の先頭の文字と末尾の文字の間に文字 "-" を配置します。 これにより、最初の文字の数値以上で、最後の文字の数値以下の数値を持つすべての文字が、セットに追加されます。 この追加された文字のセットは、プラットフォーム固有の文字表現に依存することに注意してください。 文字 "-" が、角かっこ表現の先頭または末尾にある場合、つまり文字の範囲の最初の文字または最後の文字である場合は、この文字自体を表します。  
  
 次に例を示します。  
  
-   "[0-7]" は文字セット { '0', '1', '2', '3', '4', '5', '6', '7' } を表します。 これはターゲット シーケンス "0"、"1" などと一致しますが、"a" とは一致しません。  
  
-   ASCII 文字エンコーディングを使用するシステムの場合、"[h-k]" は文字セット { 'h', 'i', 'j', 'k' } を表します。 これはターゲット シーケンス "h"、"i" などと一致しますが、"\x8A" や "0" とは一致しません。  
  
-   EBCDIC 文字エンコーディングを使用するシステムでは、"[h-k]" は文字セット { 'h', 'i', '\x8A', '\x8B', '\x8C', '\x8D', '\x8E', '\x8F', '\x90', 'j', 'k' } ("h" は 0x88 としてエンコードされ、"k" は 0x92 としてエンコードされる) を表します。 これはターゲット シーケンス "h"、"i"、"\x8A" などと一致しますが、"0" とは一致しません。  
  
-   "[-0-24]" は文字セット { '-', '0', '1', '2', '4' } を表します。  
  
-   "[0-2-]" は文字セット { '0', '1', '2', '-' } を表します。  
  
-   ASCII 文字エンコーディングを使用するシステムの場合、"[+--]" は文字セット { '+', ',', '-' } を表します。  
  
 ただし、ロケールに依存する範囲を使用すると、その範囲の文字は、ロケールの照合順序の規則によって決定されます。 範囲の定義で最初の文字の後、および範囲の定義で最後の文字の前に照合される文字が、セット内に含まれます。 セットには 2 個の終了文字も含まれます。  
  
### <a name="collating-element"></a>照合要素  
 照合要素は、単一の文字として扱われる複数文字シーケンスです。  
  
### <a name="collating-symbol"></a>照合シンボル  
 角かっこ表現の照合シンボルは、角かっこ表現で定義されているセットに*照合要素*を追加します。 照合シンボルを作成するには"[." 照合要素を「.]」の後に続きます。  
  
### <a name="control-escape-sequence"></a>制御エスケープ シーケンス  
 制御エスケープ シーケンスは、円記号の後に、文字 "c"、その後に文字 "a" ～ "z" または "A" ～ "Z" のいずれかが続きます。 その文字の名前が付けられた ASCII 制御文字と一致します。 たとえば、"\ci" はターゲット シーケンス "\x09" と一致します。これは、\<ctrl-i> の値が 0x09 であるためです。  
  
### <a name="dsw-character-escape"></a>DSW 文字エスケープ  
 dsw 文字エスケープは次の表に示す文字クラスの短い名前です。  
  
|エスケープ シーケンス|等価な名前付きクラス|既定の名前付きクラス|  
|---------------------|----------------------------|-------------------------|  
|"\d"|"[[:d:]]"|"[[:digit:]]"|  
|"\D"|"[^[:d:]]"|"[^[:digit:]]"|  
|"\s"|"[[:s:]]"|"[[:space:]]"|  
|"\S"|"[^[:s:]]"|"[^[:space:]]"|  
|"\w"|"[[:w:]]"|"[a-zA-Z0-9_]"*|  
|"\W"|"[^[:w:]]"|"[^a-zA-Z0-9_]"*|  
  
 *ASCII 文字セット  
  
### <a name="equivalence-class"></a>等価クラス  
 角かっこ表現の等価クラスは、角かっこ表現で定義されているセットに、等価クラスの定義で照合要素と同じであるすべての文字と*照合要素*を追加します。 等価クラスを作成するには、"[=" の後に照合要素、その後に "=]" を使用します。 内部的には、2 つの照合要素 `elt1` と `elt2` が等価であるのは、`traits.transform_primary(elt1.begin(), elt1.end()) == traits.transform_primary(elt2.begin(), elt2.end())` の場合です。  
  
### <a name="file-format-escape"></a>ファイル形式エスケープ  
 ファイル形式エスケープは、通常の C 言語の文字エスケープ シーケンスである "\\\\"、"\a"、"\b"、"\f"、"\n"、"\r"、"\t"、"\v" で構成されます。これらは、通常の意味を持ち、それぞれ円記号、アラート、バックスペース、フォーム フィード、改行、復帰、水平タブ、および垂直タブを意味します。 `ECMAScript` では、"\a" および "\b" は使用できません  ("\\\\" は使用できますが、ファイル形式エスケープではなく、単一文字エスケープです)。  
  
### <a name="hexadecimal-escape-sequence"></a>16 進数のエスケープ シーケンス  
 16 進数のエスケープ シーケンスは、円記号と文字 "x" を前置した 2 桁の 16 進数 (0-9a-fA-F) です。 2 桁の数字によって指定される値を含むターゲット シーケンス内の文字に一致します。 たとえば、ASCII 文字エンコーディングを使用する場合、"\x41" は、ターゲット シーケンス "A" と一致します。  
  
### <a name="identity-escape"></a>単一文字エスケープ  
 単一文字エスケープは円記号に続く単一文字です。 これは、その文字と一致します。 これはその文字が特別な意味を持つ場合に必要です。単一文字エスケープを使用することにより、特別な意味が除去されます。 例:  
  
-   "a*" は、ターゲット シーケンス "aaa" と一致しますが、ターゲット シーケンス "a\*" とは一致しません。  
  
-   "a\\*" は、ターゲット シーケンス "aaa" と一致せず、ターゲット シーケンス "a\*" と一致します。  
  
 単一文字エスケープで使用される文字セットは、次の表に示すように、正規表現の文法に依存します。  
  
|文法|使用できる単一文字エスケープの文字|  
|-------------|----------------------------------------|  
|`basic`, `grep`|{ '(', ')', '{', '}', '.', '[', '\\', '*', '^', '$' }|  
|`extended`, `egrep`|{ '(', ')', '{', '.', '[', '\\', '*', '^', '$', '+', '', '&#124;' }|  
|`awk`|`extended` に加えて { '"', '/' }|  
|`ECMAScript`|識別子の一部である文字を除くすべての文字。 通常、これには、文字、数字、"$"、"_"、および Unicode のエスケープ シーケンスが含まれています。 詳細については、ECMAScript 言語の仕様を参照してください。|  
  
### <a name="individual-character"></a>個々の文字  
 角かっこ表現内の個々の文字は、角かっこ表現で定義された文字セットにその文字を追加します。 角かっこ表現内の先頭以外の任意の場所で、"^" はそれ自体を表します。  
  
 次に例を示します。  
  
-   "[abc]" はターゲット シーケンス "a"、"b"、および "c" と一致しますが、シーケンス "d" とは一致しません。  
  
-   "[abc]" はターゲット シーケンス "d" とは一致しますが、ターゲット シーケンス "a"、"b"、または "c" とは一致しません。  
  
-   "[a^bc]" はターゲット シーケンス "a"、"b"、"c"、および "^" と一致しますが、ターゲット シーケンス "d" とは一致しません。  
  
 `ECMAScript` 以外のすべての正規表現文法では、"]" が左の "[" に続く最初の文字である場合や、先頭の "^" に続く最初の文字である場合は、その文字自体を表します。  
  
 次に例を示します。  
  
-   "[]a" は、角かっこ表現の最後に "]" がないため無効です。  
  
-   "[]abc]" はターゲット シーケンス "a"、"b"、"c"、および "]" と一致しますが、ターゲット シーケンス "d" とは一致しません。  
  
-   "[^]abc]" はターゲット シーケンス "d" と一致しますが、ターゲット シーケンス "a"、"b"、"c"、または "]" とは一致しません。  
  
 `ECMAScript` では、角かっこ表現内で文字 "]" を表すために "\\]" を使用します。  
  
 次に例を示します。  
  
-   "[]a" は、角かっこ表現が空であるため、ターゲット シーケンス "a" と一致します。  
  
-   "[\\]abc]" はターゲット シーケンス "a"、"b"、"c"、および "]" と一致しますが、ターゲット シーケンス "d" とは一致しません。  
  
### <a name="negative-assert"></a>否定アサート  
 否定アサートは、その内容以外のすべてと一致します。 これは、ターゲット シーケンスの文字を使用しません。 たとえば、"(!aa)(a*)" はターゲット シーケンス "a" と一致し、キャプチャ グループ 1 をサブシーケンス "a" に関連付けます。 ターゲット シーケンス "aa" やターゲット シーケンス "aaa" とは一致しません。  
  
### <a name="negative-word-boundary-assert"></a>否定単語境界アサート  
 否定単語境界アサートは、ターゲット文字列の現在位置が*単語境界*の直後にない場合に一致します。  
  
### <a name="non-capture-group"></a>非キャプチャ グループ  
 非キャプチャ グループは正規表現文法の 1 つの単位として内容をマークしますが、対象のテキストにラベルを付けません。 たとえば、"(a)(:b)*(c)" はターゲット テキスト "abbc" と一致し、キャプチャ グループ 1 をサブシーケンス "a" に、キャプチャ グループ 2 をサブシーケンス "c" に関連付けます。  
  
### <a name="non-greedy-repetition"></a>繰り返しの最短一致  
 繰り返しの最短一致は、パターンに一致するターゲット シーケンスの最も短いサブシーケンスを使用します。 繰り返しの最長一致では、最も長いものを使用します。 たとえば、"(a+)(a*b)" はターゲット シーケンス "aaab" と一致します。 繰り返しの最短一致を使用する場合、これはキャプチャ グループ 1 をターゲット シーケンスの先頭にあるサブシーケンス "a" に、キャプチャ グループ 2 をターゲット シーケンスの最後にあるサブシーケンス "aab" に関連付けます。 最長一致を使用する場合、これはキャプチャ グループ 1 をサブシーケンス "aaa" に、キャプチャ グループ 2 をサブシーケンス "b" に関連付けます。  
  
### <a name="octal-escape-sequence"></a>8 進数のエスケープ シーケンス  
 8 進数のエスケープ シーケンスは、円記号を前置した 1 桁、2 桁、または 3 桁の 8 進数のシーケンス (0-7) です。 これらの数字によって指定される値を含むターゲット シーケンス内の文字に一致します。 すべての桁が "0" の場合、シーケンスは無効です。 たとえば、ASCII 文字エンコーディングを使用する場合、"\101" は、ターゲット シーケンス "A" と一致します。  
  
### <a name="ordinary-character"></a>通常文字  
 通常文字は現在の文法で特別な意味を持たない、任意の有効な文字です。  
  
 `ECMAScript` では、次の文字が特別な意味を持ちます。  
  
-   ^  $  \  .  *  +    (  )  [  ]  {  }  &#124;  
  
 `basic` および `grep` では、次の文字が特別な意味を持ちます。  
  
-   」を参照してください。   [   \  
  
 また、`basic` と `grep` では、特定のコンテキストで使用されたときに、次の文字が特別な意味を持ちます。  
  
-   "*" は、正規表現の最初の文字や正規表現の先頭の "^" に続く最初の文字である場合、またはキャプチャ グループの最初の文字やキャプチャ グループの先頭の "^" に続く最初の文字である場合を除き、いずれの場合でも特別な意味を持ちます。  
  
-   "^" は、正規表現の最初の文字である場合に特別な意味を持ちます。  
  
-   "$" は、正規表現の最後の文字である場合に特別な意味を持ちます。  
  
 `extended`、`egrep`、および `awk` では、次の文字が特別な意味を持ちます。  
  
-   をクリックします。   [   \   (   *   +      {   &#124;  
  
 また、`extended`、`egrep`、および `awk` では、特定のコンテキストで使用されたときに、次の文字が特別な意味を持ちます。  
  
-   ")" は、先行する "(" と対応する場合に特別な意味を持ちます。  
  
-   "^" は、正規表現の最初の文字である場合に特別な意味を持ちます。  
  
-   "$" は、正規表現の最後の文字である場合に特別な意味を持ちます。  
  
 通常文字は、ターゲット シーケンス内の同じ文字と一致します。 既定では、2 つの文字が同じ値で表される場合、一致と見なされることを意味します。 大文字と小文字を区別しない検索では、2 つの文字 `ch0` と `ch1` は、`traits.translate_nocase(ch0) == traits.translate_nocase(ch1)` である場合に一致します。 ロケールを区別する検索では、2 つの文字 `ch0` と `ch1` は、`traits.translate(ch0) == traits.translate(ch1)` である場合に一致します。  
  
### <a name="positive-assert"></a>肯定アサート  
 肯定アサートはその内容と一致しますが、ターゲット シーケンスの文字を使用しません。  
  
 次に例を示します。  
  
-   "(=aa)(a*)" はターゲット シーケンス "aaaa" と一致し、キャプチャ グループ 1 をサブシーケンス "aaaa" に関連付けます。  
  
-   "(aa)(a*)" はターゲット シーケンス "aaaa" と一致し、キャプチャ グループ 1 をターゲット シーケンスの先頭にあるサブシーケンス "aa" に、キャプチャ グループ 2 をターゲット シーケンスの最後にあるサブシーケンス "aa" に関連付けます。  
  
-   "(=aa)(a)&#124;(a)" は、ターゲット シーケンス "a" と一致し、キャプチャ グループ 1 を空のシーケンス (肯定アサートが失敗するため) に、キャプチャ グループ 2 をサブシーケンス "a" に関連付けます。 また、ターゲット シーケンス "aa" と一致し、キャプチャ グループ 1 をサブシーケンス "aa" に、キャプチャ グループ 2 を空のシーケンスに関連付けます。  
  
### <a name="unicode-escape-sequence"></a>Unicode エスケープ シーケンス  
 Unicode エスケープ シーケンスは、円記号と文字 "u" を前置した 4 桁の 16 進数 (0-9a-fA-F) です。 4 桁の数字によって指定される値を含むターゲット シーケンス内の文字に一致します。 たとえば、ASCII 文字エンコーディングを使用する場合、"\u0041" は、ターゲット シーケンス "A" と一致します。  
  
### <a name="wildcard-character"></a>ワイルドカード文字  
 ワイルドカード文字は、ターゲット式の改行を除く任意の文字と一致します。  
  
### <a name="word-boundary"></a>単語境界  
 単語境界は、次のような場合に発生します。  
  
-   現在の文字が、ターゲット シーケンスの先頭にあり、単語文字 `A-Za-z0-9_.` の 1 つである。  
  
-   現在の文字位置がターゲット シーケンスの末尾を超えており、ターゲット シーケンスの最後の文字が単語文字の 1 つである。  
  
-   現在の文字が単語文字の 1 つであり、直前の文字が単語文字ではない。  
  
-   現在の文字が単語文字の 1 つではなく、直前の文字が単語文字である。  
  
### <a name="word-boundary-assert"></a>単語境界アサート  
 単語境界アサートは、ターゲット文字列の現在位置が*単語境界*の直後にある場合に一致します。  
  
##  <a name="matchingandsearching"></a> 一致と検索  
 正規表現がターゲット シーケンスに一致するには、正規表現全体がターゲット シーケンス全体に一致する必要があります。 たとえば、正規表現 "bcd" は、ターゲット シーケンス "bcd" およびターゲット シーケンス "bcd" と一致しますが、ターゲット シーケンス "abcd" やターゲット シーケンス "bcde" とは一致しません。  
  
 正規表現の検索が成功するには、ターゲット シーケンス内のどこかに正規表現と一致するサブシーケンスが含まれている必要があります。 検索では、通常、最も左にある一致するサブシーケンスが検出されます。  
  
 次に例を示します。  
  
-   ターゲット シーケンス "bcd" で正規表現 "bcd" を検索すると成功し、シーケンス全体と一致します。 ターゲット シーケンス "abcd" で同じ検索を実行した場合も成功し、最後の 3 文字と一致します。 ターゲット シーケンス "bcde" で同じ検索を実行した場合も成功し、最初の 3 文字と一致します。  
  
-   ターゲット シーケンス "bcdbcd" で正規表現 "bcd" を検索すると成功し、最初の 3 文字と一致します。  
  
 ターゲット シーケンス内のある場所で、一致するサブシーケンスが複数見つかった場合、一致パターンを選択する方法が 2 つあります。 *最初の一致*は、正規表現が一致すると、最初に見つかったサブシーケンスを選択します。 *最長一致*は、その場所で一致するサブシーケンスから最も長いサブシーケンスを選択します。 最も長いサブシーケンスが複数ある場合、最長一致では、最初に見つかったサブシーケンスが選択されます。 たとえば、最初の一致を使用する場合、ターゲット シーケンス "abcd" で正規表現 "b&#124;bc" を検索すると、代替の左側の項がそのサブシーケンスに一致するため、サブシーケンス "b" と一致します。したがって、最初の一致では、代替の右側の項は試行されません。 最長一致を使用する場合、同じ検索を実行すると "bc" と一致します。これは "bc" が "b" よりも長いためです。  
  
 部分一致は、正規表現の末尾に到達しない場合でも、一致が失敗せずにターゲット シーケンスの最後に到達した場合、成功します。 したがって、部分一致が成功した後、ターゲット シーケンスに文字を付加すると、その後の部分一致が失敗することがあります。 ただし、部分一致が失敗した後、ターゲット シーケンスに文字を付加しても、その後の部分一致を成功させることはできません。 たとえば、部分一致 "ab" は、ターゲット シーケンス "a" と一致しますが、"ac" とは一致しません。  
  
##  <a name="formatflags"></a> 書式指定フラグ  
  
|ECMAScript の書式規則|sed の書式規則|置換テキスト|  
|-----------------------------|----------------------|----------------------|  
|"$&"|"&"|正規表現全体と一致する文字シーケンス (`[match[0].first, match[0].second)`)|  
|"$$"||"$"|  
||"\\&"|"&"|  
|"$`" (ドル記号とそれに続く逆引用符)||正規表現と一致するサブシーケンスの直前の文字シーケンス (`[match.prefix().first, match.prefix().second)`)|  
|"$'" (ドル記号とそれに続く単一引用符)||正規表現と一致するサブシーケンスの直後の文字シーケンス (`[match.suffix().first, match.suffix().second)`)|  
|"$n"|"\n"|位置にあるキャプチャ グループと一致する文字シーケンス`n`ここで、 `n` 0 から 9 までの数値です (`[match[n].first, match[n].second)`)|  
||"\\\n"|"\n"|  
|"$nn"||位置にあるキャプチャ グループと一致する文字シーケンス`nn`ここで、`nn`は 10 ~ 99 の数値 (`[match[nn].first, match[nn].second)`)|  
  
## <a name="see-also"></a>関連項目  
 [C++ 標準ライブラリの概要](../standard-library/cpp-standard-library-overview.md)


