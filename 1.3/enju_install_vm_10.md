---
layout: page
title: 第10章 その他（カスタマイズなど） - Next-L Enju インストールマニュアル（VirtualBox編）
title_short: 第10章 その他（カスタマイズなど）
group: enju_install_vm
version: 1.3
---

* Contents
{:toc}

{::comment} misc.md {:/comment}

第10章 その他（カスタマイズなど） {#section10}
========================

10-1 Enjuを運用するにあたっての留意点・注意点 {#section10-1}
-------------------------------------------------------------

Enjuサーバは，外部からネットワーク経由でアクセスすることができるサービスとして運用されます。したがって，そのセキュリティ管理などには十分に気を配る必要があります。Enjuサーバ自体は，配付時点での最新の状況に対応できるようにセキュリティ対策を講じていますが，日進月歩のネットワーク環境では，新しいネットワーク上の脅威が発生する可能性もあります。このような状況に対応するため，運用に際しては，特に以下の２つにご注意ください。

1. 最新の配付パッケージを使用すること：Enju仮想マシンファイルについても，今後，バージョンアップを重ねるたびに配付を予定しています。機能面での充実というだけではなく，セキュリティ面からも最新のパッケージを使用ください。
2. 不必要な外部からのアクセスを禁止すること：場合によっては，ファイアウォールの導入やリモートルータでのフィルタリングについても検討した方が良いこともあるでしょう。

10-2 「条件を詳しく指定して検索」の画面をカスタマイズする {#section10-2}
-----------------------------------------------------------------------

Enju 「条件を詳しく指定して検索」の画面をカスタマイズする方法を説明します。
設定する画面がないため、これはサーバー上の作業をする必要があります。

#### 1. 念のため[「8-1 Enjuの停止」](enju_install_vm_8.html#section8-1)を実行します。

#### 2. 以下のファイルをダウンロードし、中身を編集します。

[https://github.com/next-l/enju_leaf/blob/1.3/app/views/page/advanced_search.html.erb](https://github.com/next-l/enju_leaf/blob/1.3/app/views/page/advanced_search.html.erb)


#### 3. インストールしてあるEnjuに、ディレクトリを作成します。

        $ mkdir -p app/views/page

#### 4. 2のファイルを3で作成したディレクトリにコピーします

#### 5. [「8-3 Enjuを再起動」](enju_install_vm_8.html#section8-3)を実行します。

#### 6. 画面を確認します。修正が必要なら 4.のファイルを修正し、5と6 の手順を行います。

10-3 トップの画面の検索フォームをカスタマイズする {#section10-3}
-----------------------------------------------------------------------

Enju トップの画面の検索フォームをカスタマイズする方法を説明します。
設定する画面がないため、これはサーバー上の作業をする必要があります。

#### 1. [10-2節](#section10-2) の 1. と同様です

#### 2. 以下のファイルをダウンロードし、中身を編集します。

[https://github.com/next-l/enju_leaf/blob/1.3/app/views/page/_search_form.html.erb](https://github.com/next-l/enju_leaf/blob/1.3/app/views/page/_search_form.html.erb)

#### 3. インストールしてあるEnjuに、ディレクトリを作成します。

        $ mkdir -p app/views/page

#### 4. [10-2節](#section10-2) の 4. ～　6. と同様です。

10-4 検索結果一覧画面の検索フォームをカスタマイズする {#section10-4}
-----------------------------------------------------------------------

Enju 検索結果一覧画面の検索フォームをカスタマイズする方法を説明します。
設定する画面がないため、これはサーバー上の作業をする必要があります。

#### 1. [10-2節](#section10-2) の 1. と同様です

#### 2. 以下のファイルをダウンロードし、中身を編集します。

<https://github.com/next-l/enju_biblio/blob/1.3/app/views/manifestations/_index_form.html.erb>

#### 3. インストールしてあるEnjuに、ディレクトリを作成します。

        $ mkdir -p app/views/manifestations

#### 4. [10-2節](#section10-2) の 4. ～　6. と同様です。

10-5 検索結果一覧画面に表示項目を追加する {#section10-5}
--------------------------------------------------------

Enju 検索結果一覧画面に表示される書誌情報や所蔵情報の表示内容をカスタマイズする方法を説明します。
設定する画面がないため、これはサーバー上の作業をする必要があります。

#### 1. [10-2節](#section10-2) の 1. と同様です

#### 2. 以下のファイルをダウンロードし、中身を編集します。

<https://github.com/next-l/enju_biblio/blob/1.3/app/views/manifestations/_manifestation.html.erb>

例えば、件名などを追加表示したい場合は以下のようなコード片を挿入します:

```ruby
  <%- manifestation.subjects.each do |subject| -%>
    <%= link_to "#{subject.subject_heading_type.display_name.localize}: #{subject.term}", manifestations_path(query: "subject_sm:\"#{subject.term}\"") -%>
  <%- end -%>
```

#### 3. インストールしてあるEnjuに、ディレクトリを作成します。

        $ mkdir -p app/views/manifestations

#### 4. [10-2節](#section10-2) の 4. ～　6. と同様です。


10-6 トップ画面やヘルプなどに表示する画像を置く {#section10-6}
--------------------------------------------------------------

#### 1. 置きたい画像を用意します。（ここでは例として logo.png とします）

#### 2. インストールしてあるEnju の app/assets/images/ 以下に画像ファイルを置きます。※ custom フォルダを作成し、その下にファイルを置くことを推奨します。

<div class="alert alert-info memo" markdown="1">

【Memo】

* フォルダを作成しその下にファイルを置くことも可能です。
* ファイル名やフォルダ名は任意に作成できます（ただし、Enjuが使用するものと衝突する場合は動作保証しかねます）。
* customフォルダ以下のファイルはEnjuが用意した画像と衝突しないことが保証されます。

</div>

#### 3. 以下のコマンドを実行します。

        $ bundle exec rake assets:precompile

#### 4. 参照するURLについて

以下のようなURLになりますのでこのURLを使って参照することができます。

* app/assets/images/ 以下に、 custom フォルダを作成して、その下に logo.png を置いた場合
    * URL例（デモサーバー）: https://enju.next-l.jp/assets/custom/logo.png
    * URL例（仮想マシン）: http://localhost:8080/assets/custom/logo.png

※ 画像ファイルをブラウザから置けるようにする機能を開発予定です（[詳細 #1133](https://github.com/next-l/enju_leaf/issues/1113)）。
<!-- 関連 #1144 -->
 
10-7 ヘッダーをカスタマイズする {#section10-7}
-----------------------------------------------------------------------

ヘッダーをカスタマイズする方法を説明します。
現在は、ヘッダーに表示されるタイトルしか変更できないため、
たとえば、バナー画像を使いたい場合などは、
サーバー上の作業をする必要があります。

#### 1. [10-2節](#section10-2) の 1. と同様です。

#### 2. バナー画像があれば、画像ファイルをEnju に置きます。

* 画像ファイルを置く方法は、[「10-5　トップ画面やヘルプなどに表示する画像を置く」](#section10-5)を参照してください。
* 説明で使う例として：置いたファイル：custom/logo.png 
* バナー画像の大きさは 横：640ピクセル 縦：65ピクセル　にするとちょうどよいです。大きすぎるとはみ出て表示されます。

#### 3. 以下のファイルをダウンロードし、中身を編集します。

[https://raw.githubusercontent.com/next-l/enju_leaf/1.3/app/views/page/_header.html.erb](https://raw.githubusercontent.com/next-l/enju_leaf/1.3/app/views/page/_header.html.erb)

例えば、バナー画像をタイトルの代わりにつけたい場合は、以下の記述を変更します。

        <h1><%= link_to image_tag('custom/logo.png'), root_path %></h1>

{::comment}

修正前：

        <div id="library_system_name">
          <h1 class="resource_title"><%= link_to LibraryGroup.system_name(@locale), root_path, title: LibraryGroup.system_name(@locale) %></h1>
        </div>

修正後：

        <div id="library_system_name">
          <h1 class="resource_title"><%= link_to LibraryGroup.system_name(@locale), root_path, title: LibraryGroup.system_name(@locale) %></h1>
        </div>

{:/comment}

#### 4. インストールしてあるEnjuに、ディレクトリを作成します。

        $ mkdir -p app/views/page

#### 5. [10-2節](#section10-2) の 4. ～　6. と同様です。

{% include enju_install_vm/toc.md %}
