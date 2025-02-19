# Laravel8.x公式ドキュメント翻訳リポジトリ

このリポジトリはPHP Webアプリフレームワーク、Laravel8.xの公式英文ドキュメントを日本語へ翻訳しています。


This is a Japanese translation repository for Laravel 8.x official documentations.

> 注意：Laravel開発者のTaylor Otwell氏は、英語のネイティプスピーカーです。英語しか理解できません。
> 自分の理解できないものには責任が持てないと言う理由から、
> 公式ドキュメントは英語のみです。そのため、**日本語翻訳を「公式」と呼ばないでください**。
> 「日本語ドキュメント」、「和訳翻訳ドキュメント」など適切にお呼びください。

### 誤訳／タイポなどの報告

**バージョン８.xの翻訳も本体のリポに合わせメンテは終了しました。**

* 誤訳やタイポ、未翻訳部分などを報告する場合、以下の内容を含めてください。
    * ページ（章）：GitHubのリポジトリやreadouble.comのURL、もしくはページのタイトル（「キュー」、「認証」）など。ページの特定が容易であれば形式はかまいません。（報告に手間がかかるので、行番号を含めたリンクをわざわざ張る必要はありません。）
    * 問題のある和文、および正しいと思われる和文（エディターで検索して該当箇所を見つけます。）
* 専門用語（訳語）の不統一に関しては、プロジェクト全体を検索しますので、特定のページを指定する必要はありません。それ以外の表記揺れに関しては、該当ページがわかるようにしてください。（表現上の揺れなどは、一度に変更できません。少しづつ、気がついた時点で修正します。）
* 日本語ドキュメントを利用するのは日本人です。そのため、報告やコメントは日本語で記述してください。
* このリポジトリでは8.xの翻訳和文のみ管理しています。readouble.comで公開している他のバージョンの和文に関しては、@HiroKwsにツイートいただくか、hirokws@gmail.comへご連絡ください。なお、メンテナンス期間をフレームワーク本体と合わせているため、readouble.comで公開している日本語翻訳の旧バージョンは更新していません。バージョン8.xリリース時点で、メンテ対象の和文バージョンは6.xLTSとこの8.xです。

#### issueで報告する場合

Issueで報告していただくのが、一番簡単です。

<https://github.com/laravel-ja/ja-docs-8.x/issues>のページで、"New issue"ボタンをクリックし、issueを発行してご報告ください。

> 2ndパーティーパッケージとして取り入れられたCashier-mollieのドキュメントは、オリジナル英語並びに本翻訳リポジトリに含まれていません。そもそもCashierのドキュメント利用者は少ないため、mollieドキュメントなど3rdパーティパッケージの説明はゆっくりと翻訳していきます。翻訳中は誤訳などのレポートはご遠慮ください。

#### プルリクエストで報告する場合

* translation-jaディレクトリ下の日本語翻訳Markdownファイルのみを変更してください。それ以外のファイルは変更しないでください。
* 翻訳対象となるバージョンの原文は、original-enディレクトリ下にあります。Laravelのドキュメントリポの最新版ではないことに注意してください。
* ディレクトリ／ファイル構造を変更しないでください。
* 原文と翻訳の文章構造は一致させてください。原文と翻訳は、空行・タイトル行など行ごとの構造を同一に保っています。これにより、翻訳が原文のどの箇所であるかを簡単に見つけることができます。また、原文の変更を翻訳へ反映させる処理を自動化するにも役立てています。
* 原文／翻訳間のファイル構成の一致のチェック、原文／翻訳間の各ファイルの行構成の一致のチェック、用語の不一致のチェックを行うスクリプトが、scripts/pre-commitです。可能であればこれをコミット前に実行し、確認してください。実行にはgawk、awk、sed、bashなどが必要です。
* pre-commitは、プルリクエスト時にCIでも実行されています。エラーになるものはマージしません。


### ディレクトリ構造

| ディレクトリ／ファイル  | 内容                               |
| ----------------------- | ---------------------------------- |
| original-en    | 翻訳対象原文ブランチの内容                  |
| translation-ja | 日本語翻訳Markdownファイル                  |
| scripts        | 用語統一、文章構造確認などの補助スクリプト   |


### タグ

| タグ形式               | 内容                                                       |
| ---------------------- | -----------------------------------------------------------|
| published.YYMMDD.HHMM  | readouble.comへ公開したコミット                            |

`published.YYMMDD.HHMM`形式のタグは、readouble.comなどで翻訳文を読む利用者向けのタグです。この形式のタグ間でdiffを確認してもらうことで、前回のリリース時の原文／翻訳文と次回の変更点／差分を確認できます。

### メンテナンス期間

原則、Laravel8.xのメンテ期間である半年。次回のバージョンのリリースまで。２０２１年３月８日までの予定です。

メンテ作業が煩雑になった場合は、期間途中でもリポジトリを閉じます。あらかじめご了承ください。

### メンテナンス方針

日本語翻訳の構造は英語と一致させています。行単位でも一致させています。これにより、原文の変更点の和文への適用などを自動化しています。また、行で対応させることにより、日本語訳に対する英文を見つけ出しやすくしています。

重大な原文の間違いがない限り、和文に情報を付け加えません。LaravelメンテナのTaylor Otwell氏は、「ドキュメントに何もかも詰め込んでしまうと、メンテしづらく、読み手にも負担になる」という方針です。その方針を基準に現在の情報量となっています。それを尊重しています。

以前は日本語訳にいろいろと注釈を付け加えていましたが、長期間のメンテナンスでは管理が負担になります。作業をシンプルに保たないと長期間のメンテナンスは困難です。その理由でも、原則注釈は付け加えていません。

日本語訳に足りない部分は、原文に足りない部分です。公式ドキュメントに足りない部分を追加するPRを行うか、もしくはブログ記事などを書き、内容を補ってください。また、原文の間違っている箇所、わかりづらい箇所に付きましては、原文のリポジトリへの報告や修正依頼をお願いします。

### 翻訳方針

翻訳が必要なのは、英語が苦手な方です。「英語を読むことが苦手な技術者」をターゲットとして翻訳しています。そのため、訳語が日本のコミュニティで定まった用語は、それを尊重しています。英単語が技術用語として定着している言葉は、日本語読みを採用しています。（リクエスト、イベントなど）また、まだ適切な用語が存在しない部分についても、米語発音を基本に訳語として採用しています。

初学者に対して読みやすくすることは、学習を終えたレベルの技術者にとって冗長になります。当翻訳を必要とされる方は、初学者よりベテラン開発者のほうが多いかと思います。そのため、初心者に優しくするよりは、ある程度のレベルの技術者であれば親しんでいる、もしくは調べれば意味の取れる専門用語レベルを選んでいます。

バリデーションの一覧表記などは、原文のままが良いと言う意見があります。私も翻訳し直す機会ごとに、訳すのか原文のままにするか判断しています。現時点の判断では、基本的な方針に従い、専門的（コンピューター／数学分野／ソフト開発業界用語）な用語に訳しています。

訳出の変更などのissueは、「英語を読むのが苦手な技術者」の視点で検討してください。issueを発行してくださる方は、英語を読める方が多く、翻訳を公式ドキュメントの補助として利用している方も多いでしょう。私自身もそう利用していますが、原則は補助として利用する目的でなく、英語の公式ドキュメントを読解するのが困難な技術者の手助けにしていただくのが方針です。

### 翻訳方法

２０２０年９月頃からメンテナのTaylor Otwell氏がちょくちょく原文を修正しだし、１２月頃に改定に集中しているツイートがあり、数週間後にまとめて改訂版がリリースされました。

その量は改定ファイル数や改定行数共に元の９５％を超える量のため、全文翻訳し直しが必要になりました。

当初は人力での翻訳をしていましたが、補助で使いだしていたGoogle翻訳が日に日に精度を上げ、Laravel関係のドキュメントであればほぼ内容を理解できるところまで成長していました。精度をあげるには学習データが必要です。readouble.comはURLの一部を変えるだけで日英が切り替わり、しかも英文と和文が行（パラグラフ）単位で１：１ですので、大量のデータを収集するには便利です。推測ですが学習データとして利用されていると思います。それが確信できるのは、約語と文章のクセです。

公式ドキュメント以外でも、Laravel関係のドキュメントであれば、Google翻訳でかなり良い文章に訳されると思います。約語は私の訳の日本語が選ばれる確率がだいぶ高いことが観察されると思います。

そして、Laravelドキュメント翻訳は長年に渡るプロジェクトで、当初は原文の宣伝文ぽい雰囲気を生かすため、テレビショッピングのような文章に訳していました。段々とLaravelコミュニティの成長と技術的な牽引役を担うに伴い、文章も段々とフォーマルに変化していきました。それに合わせ、訳語も段々とフォーマルに切り替えていきました。その過程で、文章のフォーマルさの程度が合わなくなっている部分も出てきました。

そこで文調を統一するためにも、今回からGoogle翻訳の訳語をベースにして、誤訳部分や不自然な部分を修正するという方針に切り替えました。これで、全文を訳し直せば、語調は統一できます。（機械翻訳ぽさは入り込みますが、統一されていれば慣れてしまいます。実用には支障ありません。そもそも、大量に翻訳していくと、日本語がバタ臭くなり、それが普通で自然ではないことに気が付かなくなりがちです。）

全文の改訳作業中も日々翻訳精度は進化していってます。公式ドキュメント以外の英文ドキュメントも簡単に参考にできる時代になりました。

### 参照について

原文と当翻訳のライセンスはMITです。Copyrightは存在しています。そのため、参照する場合は参照元を記述するか、リンクを張る必要があります。（日本の著作権法による）

原文と当翻訳は別のCopyrightです。そのため、原文と当日本語訳を参照する場合は、それぞれの参照元を示す必要があります。（日本の著作権法による）

技術者としての知識とコンプライアンス精神を表すために、他のMITライセンスのプロジェクトからドキュメントなど一部を記事などから参照し、公開する場合もきちんと参照元を示しましょう。忘れがちですが動画、ポッドキャストでも同様です。
