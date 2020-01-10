# どう報告すればいいのか分からない

# [フィードバック] OSSへのフィードバックには何をどう書けばいいのか、どのプロジェクトに報告すればいいのか

※注：この記事の対象読者は、「OSSを使用していてトラブルに遭遇しているか、改善の提案があり、その情報を開発元のイシュートラッカーに伝えようとしているが、どんな内容を書けばよいかわからない」という人です。そもそも「どこに報告すればよいかわからない」「イシュートラッカーに書き込んでいいかどうか不安がある」という方は、[1つ前の記事](20190618)をご参照下さい。


結城です。

[1つ前の記事](20190618)では、フォーラムとイシュートラッカーのどちらに書き込めばよいかわからない場合の考え方について詳しく語りました。その際、両者の目的の違いを以下のようにまとめました。

* フォーラム：*個人の問題の解決*を図る場所。
* イシュートラッカー：*ソフトウェアの問題の解決、品質の向上*を図る場所。

この記事ではその続編として、イシュートラッカーの目的から導かれる「適切な、書くべき報告の内容」を語ってみます。


## 書くべき内容、避けるべき内容

フォーラムとイシュートラッカーの目的の違いは、「投稿する内容をどうまとめればよいのか」という事を考える時の指針にもなります。「ソフトウェアの問題の解決」を目的とするイシュートラッカーに報告する内容は、その目的に沿って、「ソフトウェアの開発に関わる人達が、このソフトウェアの問題を解決するには、どのような情報が必要か？」という視点で整理する事になります。

例えば、以下の3項目は典型的な「書くべき内容」です。

* *Steps to reproduce：現象の発生条件、再現に必要な手順*。
  - 他の人は、どうすればその現象が起こるかを知らないし、あなたが普段どのようにその機能を使っているのかも知らないので、あなたが詳しく説明するしかありません。
  - メニューの選び方、機能の呼び出し順序など、あなたが無意識でしている操作の仕方がその現象を引き起こす決定的なきっかけとなっているかもしれません。
* *Actual result：実際に起こる結果*。
  - 他の人は、自分の環境で得られた結果が、あなたの見ている物と同じかどうか分からないので、あなたが詳しく説明するしかありません。
* *Expected result：本来期待される結果*。
  - 他の人は、あなたほどにはその機能や使い方の事を詳しく知らないかもしれないので、あなたが詳しく説明した方が効率がよいです。


*その問題のせいで自分がいかに困っているか？ という訴えは報告のメインの内容とはなり得ません*。プロジェクト全体の中でその問題の重要度の高さを認識してもらうための材料として、問題の影響度・深刻さの説明としてそれらの訴えを盛り込む場合はありますが、そのような訴え自体が問題の原因究明や修正箇所の特定に役立つという事は、基本的には無いからです。


## 重複する報告も、場違いな報告も、無駄じゃないのでしていい

しかし、いざ報告しようとしても、

* 既に他の人が報告しているにもかかわらず、自分の探し方が下手なだけで、既存の報告を見つけられていないだけかもしれない。
* この問題をこのプロジェクトに報告するのが適切かどうか分からない。もっと適したプロジェクトがあるかもしれない。場違いな報告をしたら迷惑かもしれない。

という心配から報告をためらう、という事例はワークショップの中でもよくあります。筆者はそのような場合には、「不安を感じるくらいなら、自分が思う内容・表現のままでそのプロジェクトに報告してしまってよい」とアドバイスする事が多いです。

既知の報告がないか全く調べていない、というのはさすがにまずいですが、*自分の思いつく表現で検索して報告が見つからないなら、その表現で報告して大抵は問題ありません*。なぜなら、仮にその後既知の他の報告と重複していると分かって、そちらに誘導された上でクローズされたとしても、その報告内容自体が、*同じ探し方をする人のための今後の誘導になるから*です。

適切な報告先プロジェクトかどうか分からない、という場合も同様です。その問題が根本的には別のソフトウェアの問題だったと後から分かっても、*同様の現象に遭遇した人のための誘導になる*ので、報告は無駄にはなりません。例えば1つ前の記事で紹介した事例では、今後同様の現象に見舞われて検索して辿り着いた人は、今後はMicrosoft IMEの動向に注意するとよい、という情報を得られる事になります。

また、根本的な原因については既に報告があったとしても、その報告で触れられている以外の現象の情報があると、それは問題の影響度合いを示す情報になります。当初の報告では些細な問題だから後回しにしようと判断されていた物が、実はユーザーレベルで大きな影響を受ける物だったと分かって、*対応の重要度・緊急度が引き上げられる*という事は度々あります。

## 却下された報告や提案にも価値がある

明らかな不具合というよりは「こうなっているとより良い」という提案の性質が強い報告の場合に多いのですが、「それは対応しない」「やらない」と判断され却下される場合もあります。そのような場合も、「無駄だった」「失敗した」という考え方をする必要はありません。というのも、「ある提案が却下された」という事そのものにも意義があるからです。

OSSのプロジェクトのスコープ[^scope]は、必ずしもすべて明確化されているとは限りません。ある人にとっては「当然あるべき」と思える機能が無かったり、逆に、「無駄にしか思えない」という機能があったり、特に、それについて何の説明も無いという事はざらにあります。大規模なプロジェクトでは、すでに参加している人の間ですら解釈が別れていたりもします。

[^scope]: プロジェクトとして取り組む事の範囲。

しかし、例えスコープが明文化されていなくても、一貫性を持った数々の判断の結果、その輪郭は段々と浮かび上がってきます。新たな判断の事例が1つ増えるという事は、*不明瞭だった基準がより明確化されたという事になり、後から来た人にとって有用な情報となります*。また、判断と共にその根拠が示されていれば、後になって状況が変わり根拠が薄れた時などに、それを理由として再考を求める事もできます。

そのような意義ある判断を引き出すためにも、*議論は「自分の意見を押し通すため」ではなく「プロジェクトの目的をより良く達成するため」という点を念頭に置いて、「相手（敵） v.s. 自分」ではなく「問題 v.s. プロジェクト」という方向で行いましょう*。反論も、主張の材料を補ったり、説明しきれていなかった理由を追加で説明したりと、意味のある反論をする事が肝要です。感情的に同じフレーズを繰り返すだけや、明確な根拠無しに強弁するだけのような不誠実な態度、他の参加者の共感を得られないゴリ押しは、百害あって一利無しです。

ただし、*実際に手を動かす人が足りないから労力的に対応できないという理由で却下される場合は、より深く関わるチャンスです*。自分で実装してパッチ（プルリクエスト）を提出し、その後もメンテナンスを引き受け続ければ、あなたも立派に開発者の仲間入りという訳です。


## 「対案」無しでも報告・提案していい

* 報告だけでは無責任なのではないか？ 対案まで考えてから出さないと駄目なんじゃないか？
* パッチ（プルリクエスト）まで書いて初めてOSS開発への参加と言えるんじゃないか？

といった点で悩んで報告をためらう、というケースもあります。筆者はこのような場合、「対案は無くてもいいから、まず報告してみよう」とアドバイスします。

もちろん、コードのレベルで修正の仕方まではっきり分かっているのなら、パッチやプルリクエストの形でフィードバックできるに越した事はないです。しかし、そうできないならフィードバックしない方がよい、という事はありません。

むしろ、自分の考えつく解決策が最良であるとは必ずしも限りません。詳しい事情が分かっていない段階で自分の思い込みだけで独りよがりに実装を作り込んでしまうと、その労力がまるっきり無駄になるという事もあり得ます。例えば、ある機能の不具合を見つけて、その問題を解消するための複雑な変更を持ち込んだが、単にその機能全体を既存の別ライブラリで置き換えれば済む事だった、というような事はよくあります。筆者も、過去に[強引な実装のパッチを代理で投稿してもらった事がありました](https://bugzilla.mozilla.org/show_bug.cgi?id=61846 "61846 - Undockable My Sidebar - in a new window")が、実装の筋が悪すぎたためか、それ以上話が進む事はありませんでした。

イシュートラッカーは「問題の解決」に取り組むための場であって、「特定の解決策の実現」に取り組む場ではありません。解決策は関わる人みんなで考えてよく、一人で抱え込む必要はないのです。よく「文句を言うなら対案を示すべき」という言い方がされますが、だからといって「対案が無いなら文句を言ってはならない」は真ではありません。*問題解決に取り組む1つのチームの一員として、対案を考える事も含めて皆で取り組む*、という姿勢・考え方をするのがポイントです。


## 同じ問題に取り組む仲間と思って接しよう

真摯に議論しようという話とも共通しますが、「問題を解決する開発者達 v.s. 外部から善意で協力しているただのユーザーの自分」という壁を自ら作る事は避けた方がよいです。対等な関係ではないという事を過剰に意識してしまうと、実際以上に大きな上下関係を自分の中に作り上げてしまい、コミュニケーションの妨げになります。

[1つ前の記事](20190618)ではOSSに新たに関わる人を新入社員に例えましたが、そう考えれば、なぜ自分とプロジェクトの間に過度に壁を作るべきでないのかが分かるのではないでしょうか。新メンバーがお客様気分で上げ膳据え膳に期待してふんぞり返るのはおかしいですし、かといってへりくだりすぎるのもおかしいですよね。

無論、雇用されフルタイムで開発に従事している人と、外部から余力の範囲で関わっている人の間では、立場も権限も異なります。しかし、そのプロジェクトの目的、あるいは報告した1つの問題の解決に向けて一緒に取り組む仲間という点では差は無いはずですから、お互いに敬意を持って接する事が大事です。

特に、*「自分は問題で損をした被害者なんだ。その被害者自身がわざわざ協力してやってるんだ。だからお膳立てはあいつらの方で整えてくれて然るべき」というような捉え方は、問題の解決を遠のけさせこそすれ、近づけさせは決してしません*。このような意識を強く持ってしまうと、相手の無理解を責めたり相手をやり込めたりする事にばかり意識が向いてしまい、ひいては特定個人に対する罵倒や中傷にまでエスカレートし得ます[^mistake][]。

[^mistake]: お恥ずかしい話ですが、筆者も何度かこれで失敗しています。

## まとめ

以上、OSSにフィードバックする事に不慣れな場合に悩みがち・判断に迷いがちと思われる点について、イシュートラッカーの目的から導かれる「適切な考え方」を、筆者の感覚から語ってみました。

表現を変えながら繰り返し何度か述べていますが、*OSS開発に関わる際は基本的に「問題 v.s. それに立ち向かうプロジェクト参加者達（そして、その一員としての新人の自分）」という構図で考え取り組む事が大事だ*というのが、筆者の考えです。かつては思ったように成果を出せなかった自分も、そのように考えられるようになって以降は、より有用な報告ができ、提出したパッチやプルリクエストを取り込んでもらえる機会も増えたように思います。まだOSSの開発への参加に不慣れで、報告がうまくいかなくて悩んでいるという方は、この記事で述べた点を意識してみてはいかがでしょうか？

また、この記事で述べた事は実際にはOSSに特有の話ではなく、一般的に企業内でバグ票をやり取りするような場合にも共通して言える事です。[1つ前の記事](20190618)ではOSSのイシュートラッカーを出入り自由の社屋や工場に例えましたが、OSS開発の場で広く共有されているノウハウの中には、普通に仕事の上で有用な物も多く含まれています。特に、OSS開発では「多くの人を雇って人海戦術で乗り切る」というような力業での解決が難しいため、いかに少ないコストで最大の効用を得るかという点で工夫がなされている事も多いです。当社のOSS開発支援サービスでは、[OSS開発に参加していきたいという企業さまのお手伝い](20190529)だけでなく、[OSSコミュニティでの開発ノウハウを企業内での開発に活かすお手伝い](20181112)も承っています。そういった事に関心をお持ちの担当者さまがいらっしゃいましたら、ぜひ[お問い合わせフォーム](/contact/)よりご連絡下さい。
