# はじめに

「#駆け出しエンジニアと繋がりたい」というハッシュタグを巡って、初級者と中・上級者の間で断絶が起こっています。「技術的な知見を身に着けて成長したいけど、どこから取り組めばいいか分からないので、同じ悩みを抱える人同士で連帯したい」という人達がいる一方で、ベテランの方々は「駆け出し同士で繋がっても意味なくない？」と冷めた見方をしている、そんな構図であるように筆者の目には見えています。

「駆け出しエンジニア」というレベルから脱して中・上級者になる道は、プログラミングスクールだけではありません。本書で紹介する、世の中に無数にある「OSS開発の現場」には、*先達の助けを得ながら実際の世界を少しずつ良くしていく*という体験があり、スクールとはまた違った活きた学びが満ちています。

ですが、「OSS開発には誰でも参加できる」とはよく言われるものの、実際に参加している人は少数派です。OSSプロジェクトの側は門戸を開いているつもりなのですが、その門をくぐって「OSSを使う人」から「OSS開発に関わる人」になるためには、学びを目的とする人に限らず「OSS開発に関わりたい」という動機を持つさまざまな人にとって、どうもなかなか越えられない心理的なハードルがあるようです。

本書はそのようなハードルを取り払い、OSSを使うだけという立場から一歩先に進んで、「OSS開発に参加して改善に協力する」「OSSへ有意義なフィードバック[^feedback]をする」側、いわゆるコントリビューター[^contirbutor]になるための方法や考え方を紹介する本です。具体的には、次に挙げるような人に役立ててもらうことを想定しています。

[^feedback]: 障害を報告したり、要望を伝えたり、パッチやプルリクエストの形でコードを提供したりすること。
[^contributor]: フィードバックを通じてプロジェクトに協力する人のこと。直訳すると「貢献者」ですが、「貢献」と言うと「滅私奉公」のような仰々しいイメージを持つ人もいるかと思いますので、本書ではカタカナ語でこのように表記することにします。

* OSSに対してしたい提案、解決したい問題があるが、そのフォードバック方法が分からなくてためらっている。
* 特に具体的なフィードバックがある訳ではないが、好きなOSSがあってそれに関わりたい、何か力になりたいと思っている。
* 最新のOSSのツールやライブラリを使って製品やサービスを作りたい。「最新版」を不具合を恐れずに使えるようになりたい。
* 技術者として学びを得て成長したい。OSSコミュニティで成果を出して一旗揚げたい。

本書の内容は、OSS開発に関わる人を継続的に増やそうという取り組みである[OSS Gate](https://oss-gate.github.io/)の中で定期的に行われている「OSS Gate東京ワークショップ」にサポーターとして参加する中で見聞きしたことや、寄せられた質問に対して答えた内容に基づいています。中には特に事実に基づいていない「意見」の域を出ない記述もありますが、筆者自身はその見解に基づいて実際にフィードバックを行っており、パッチやプルリクエストもマージしてもらえていますので、まったく的外れな事を書いているという事はないと思われます。

OSS Gateでは「OSSへのフィードバック経験が豊富な人の助けを得ながら、初めてのフィードバックを実際にやってみる」という趣旨のワークショップを定期的に東京エリアで開催しています。また、東京以外にも京都、大阪、広島、札幌の各エリアでも現地の有志によるワークショップの開催実績があり、全体では2016年から2020年1月の間で計70回近く開催されています。本書を読んだ後でも独りでフィードバックするのは怖くてためらわれるという場合には、他の人と助け合いながら落ち着いてフィードバック体験ができますので、OSS Gateワークショップに足を運んでみて下さい。また、初めてのフィードバックを実際にやってみて自信が付いたら、次のワークショップへサポーターとして参加して、OSSにフィードバックしてみたい後進の人の手助けをしてみて頂ければ幸いです。

本書によってOSSへフィードバックできる人が増えて、世の中の問題が一つでも多く解決される事に繋がってくれれば、なによりです。
