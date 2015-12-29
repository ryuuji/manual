---
layout: page
title: 初期設定マニュアル - Next-L Enju初期設定マニュアル
title_short: 第5章 各種形態や状態等に関するシステム設定を行う
group: enju_setup
version: 1.2
---

* Contents
{:toc}

第5章 各種形態や状態等に関するシステム設定を行う {#section5}
============================================================

Enjuの利用を始めるにあたり，形態・状態等に関するシステム設定として，次のような設定作業を行います。

* 資料の形態の作成
* 貸出状態の編集
* 言語の編集
* 利用制限の編集作成
* 発行頻度の編集作成
* 資料の関係の種類の作成

{::comment}5-1 enju_setup/carrier_type.md {:/comment}

{::comment}5-2 enju_setup/ciculaion_status.md {:/comment}

{::comment}5-3 enju_setup/language.md {:/comment}

{::comment}5-4 enju_setup/use_restriction.md {:/comment}

{::comment}5-5 enju_setup/frequency.md {:/comment}

{::comment}5-6 enju_setup/manifestation_relationship_type.md {:/comment}

5-1 資料の形態を作成する {#section5-1}
--------------------------------------

資料の形態を設定します。

* 参考文献：
  * RDA: "3.3.1.3 Recording Carrier Type"
  * LCの ["Term and Code List for RDA Carrier Types"](http://www.loc.gov/standards/valuelist/rdacarrier.html)

### 5-1-1 設定項目 {#section5-1-1}

* 名前：資料の形態を入力します。
* 表示名：画面に表示する名称を入力します。
* 資料の形態と貸出区分の関係：資料の形態と貸出区分の関係を入力します。（注：新規作成画面では設定できません。いったん、新規作成したあと、編集画面で設定します）
* 注記：注意事項や特記事項などを入力します。

### 5-1-2 設定方法 {#section5-1-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。  

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［資料の形態］をクリックします。  

![資料の形態の設定](../assets/images/image_carrier_type.png)

#### 3. 右メニューの［資料の形態の新規作成］をクリックします。

![資料の形態の設定](../assets/images/image_carrier_type_1.png)

<div class="alert alert-info memo" markdown="1">
【Memo】登録済みの資料の形態を修正したい場合は[編集]リンクをクリックします。順序を変更したい場合は、最左列の ![上矢印](../assets/images/arrow_up.png) や ![下矢印](../assets/images/arrow_down.png) をクリックすることで変更できます。
</div>

#### 4. 設定項目に必要事項を入力し、［登録する］ボタンをクリックして，設定内容を登録します。

![資料の形態の設定](../assets/images/image_carrier_type_2.png)

#### 5. 「資料の形態は正常に作成されました。」とメッセージが表示されます。貸出区分との関連付けを行うために右メニューの[編集]をクリックします（新規作成の場合、貸出区分との関連付けができないため）。

![編集](../assets/images/image_carrier_type_3.png)

#### 6. 資料の形態と貸出区分の関係の[追加]リンクをクリックします。

![資料の形態と貸出区分の関係の追加](../assets/images/image_carrier_type_4_0.png)

#### 7. 貸出区分のメニューを選びます（例では、CDを選んでいます）。

![資料の形態と貸出区分の関係](../assets/images/image_carrier_type_4.png)

<div class="alert alert-info memo" markdown="1">
【Memo】メニューに関連付けたい貸出区分がない場合は、貸出区分を新規作成します。作成方法は、「[3-5 貸出区分を設定する](enju_setup_3.html#section3-5)」を参照してください。
</div>

#### 8. 貸出区分に先ほど選択した貸出区分が表示されているのを確認します（例ではCD）。これで、資料の形態が作成できました。

![結果の確認](../assets/images/image_carrier_type_5.png)

<div class="alert alert-info memo" markdown="1">
【Memo】資料の形態と貸出区分の関係づけについては、[図書館の管理]-->[システムの設定]-->図書館の[資料の形態と貸出区分の関係]リンクをたどった先でもできます（--> 詳細：「[3-7 資料の形態と貸出区分の関係を設定する](enju_setup_3.html#section3-7)」）。
</div>

5-2 資料の内容の種別を作成する {#section5-2}
--------------------------------------

資料の内容の種別を設定します。

* 参考文献：
  * RDA："6.9.1.3 Recording Content Type"
  * LCの ["Term and Code List for RDA Content Types"](http://www.loc.gov/standards/valuelist/rdacontent.html)


### 5-2-1 設定項目 {#section5-2-1}

* 名前：資料の内容の種別を入力します。
* 表示名：画面に表示する名称を入力します。
* 注記：注意事項や特記事項などを入力します。

### 5-2-2 設定方法 {#section5-2-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［資料の形態］をクリックします。

![資料の内容の種別の設定](../assets/images/image_content_type.png)

#### 3. 右メニューの［資料の内容の種別の新規作成］をクリックします。

![資料の内容の種別の設定](../assets/images/image_content_type_1.png)

<div class="alert alert-info memo" markdown="1">
【Memo】登録済みの資料の種別を修正したい場合は[編集]リンクをクリックします。削除したい場合は、[削除]リンクをクリックします。ただし、関連する書誌レコードがあるものについては[削除]リンクは表示されず、削除できません。順序を変更したい場合は、最左列の ![上矢印](../assets/images/arrow_up.png) や ![下矢印](../assets/images/arrow_down.png) をクリックすることで変更できます。
</div>

#### 4. 設定項目に必要事項を入力し、［登録する］ボタンをクリックして，設定内容を登録します。

![資料の内容の種別の設定](../assets/images/image_content_type_2.png)

#### 5. 「資料の内容の種別は正常に作成されました。」とメッセージが表示されます。これで、資料の内容の種別が作成できました

![資料の内容の種別の設定](../assets/images/image_content_type_3.png)

5-3 貸出状態を編集作成する {#section5-3}
----------------------------------------

システムの標準設定を変更する必要がでることは基本的にはありません。 所蔵情報登録の際に表示される[貸出状態]のメニューで表示される文言や、メニューの表示順序を変更したいときのみ編集の必要がでます。

### 5-3-1 設定項目 {#section5-3-1}

* 名前：貸出状態の名称を入力します。
* 表示名：画面に表示する名称を入力します。
* 注記：注意事項や特記事項などを入力します。

### 5-3-2 設定方法 {#section5-3-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。  

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［貸出状態］をクリックします。  

![貸出状態の設定](../assets/images/image_initial_058_0.png)

#### 3. 設定したい項目の［編集］をクリックします。  

![貸出状態の編集](../assets/images/image_initial_058.png)  

<div class="alert alert-info memo">【Memo】一覧の表示順序を変更するには，表の1列目に表示されている↑または↓をクリックして行を入れ替えます。</div>

#### 4. 設定項目に必要事項を入力し、［更新する］ボタンをクリックして，設定内容を更新します。  

![貸出状態を更新](../assets/images/image_initial_059.png)  

5-4 利用制限を編集する {#section5-4}
------------------------------------

システムの標準設定を変更する必要がでることは基本的にはありません。
所蔵情報登録の際に表示される[利用制限]のメニューで表示される文言や、メニューの表示順序を変更したいときのみ編集の必要がでます。

### 5-4-1 設定項目 {#section5-4-1}

* 名前：利用制限を入力します。
* 表示名：画面に表示する名称を入力します。（入力必須）
* 注記：注意事項や特記事項などを入力します。

### 5-4-2 定方法 {#section5-4-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。  

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［利用制限］をクリックします。  

![利用制限の設定](../assets/images/image_initial_062_0.png)

#### 3. 設定したい項目の［編集］をクリックします。  

![利用制限の編集](../assets/images/image_initial_062.png)  

<div class="alert alert-info memo">
【Memo】一覧の表示順序を変更するには，表の1列目に表示されている↑または↓をクリックして行を入れ替えます。
</div>

<div class="alert alert-info memo">
【Memo】多くの利用制限が登録されてはいますが、Enju Leaf 1.1.0以下では「通常期間貸出」と「貸出不可」のみが利用できます。
</div>

#### 4. 設定項目に必要事項を入力し、［更新する］ボタンをクリックして，設定内容を更新します。  

![利用制限の更新](../assets/images/image_initial_063.png)  

5-5 人物・団体の種類を編集する {#section5-5}
------------------------------------

システムの標準設定を変更する必要がでることは基本的にはありません。
[人物・団体の新規作成や編集](enju_operation_4.html#section4-10)の際に表示される
[人物・団体の種類]のメニューで表示される文言や、
メニューの表示順序を変更したいときのみ編集の必要がでます。

### 5-5-1 設定項目 {#section5-5-1}

* 名前：人物・団体の名称を入力します。（入力必須）
* 表示名：画面に表示する名称を入力します。
* 注記：注意事項や特記事項などを入力します。

### 5-5-2 設定方法 {#section5-5-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。  

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［人物・団体の種類］をクリックします。  

![人物・団体の種類の設定](../assets/images/image_initial_agenttype_0.png)

#### 3. 右メニューの[人物・団体の種類の新規作成]をクリックします。  

![人物・団体の種類の新規作成リンク](../assets/images/image_initial_agenttype_1.png)

<div class="alert alert-info memo" markdown="1">

【Memo】修正したい場合は[編集]リンクをクリックします。
削除したい場合は，[削除]リンクをクリックします。
ただし、この種類を使った「人物・団体」があるものについては[削除]リンクは
表示されず、削除できません。 
一覧の表示順序を変更するには，
表の1列目に表示されている↑または↓をクリックして行を入れ替えます。

</div>

#### 4. 設定項目に必要事項を入力し、［登録する］ボタンをクリックして，作成します。

![人物・団体の種類の新規作成](../assets/images/image_initial_agenttype_2.png) 

5-6 言語を編集する {#section5-6}
--------------------------------

### 5-6-1 設定項目 {#section5-6-1}

* ネイティブ名：ネイティブ名を入力します。
* 表示名：画面に表示する名称を入力します。
* ISO 639-1： ISO 639-1の値を入力します。
* ISO 639-2： ISO 639-2の値を入力します。
* ISO 639-3： ISO 639-3の値を入力します。
* 注記：注意事項や特記事項などを入力します。

### 5-6-2 設定方法 {#section5-6-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。  

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［言語］をクリックします。  

![言語の設定](../assets/images/image_initial_060_0.png)

#### 3. 設定したい項目の［編集］をクリックします。  

![言語の編集](../assets/images/image_initial_060.png)  

<div class="alert alert-info memo">【Memo】一覧の表示順序を変更するには，表の1列目に表示されている↑または↓をクリックして行を入れ替えます。</div>

#### 4. 設定項目に必要事項を入力し、［更新する］ボタンをクリックして，設定内容を更新します。  

![言語の更新](../assets/images/image_initial_061.png)  

5-7 発行頻度を編集する {#section5-7}
----------------------

### 5-7-1 設定項目 {#section5-7-1}

* 名前：発行頻度を入力します。
* 表示名：画面に表示する名称を入力します。
* 注記：注意事項や特記事項などを入力します。

### 5-7-2 設定方法 {#section5-7-2}

#### 1. ［図書館の管理］メニューから［システムの設定］を選択します。  

![システムの設定](../assets/images/image_system_setup.png)

#### 2. ［発行頻度］をクリックします。  

![発行頻度の設定](../assets/images/image_initial_064_0.png)

#### 3. 設定したい項目の［編集］をクリックします。  

![発行頻度の編集](../assets/images/image_initial_064.png)

<div class="alert alert-info memo">【Memo】新規に作成したい場合は、右メニューの[発行頻度の新規作成]をクリックします。削除したい場合は、[削除]リンクをクリックします。ただし、関連する書誌レコードがあるものについては[削除]リンクは表示されず、削除できません。一覧の表示順序を変更するには，表の1列目に表示されている↑または↓をクリックして行を入れ替えます。</div>

#### 4. 設定項目に必要事項を入力し、［更新する］ボタンをクリックして，設定内容を更新します。

![発行頻度の更新](../assets/images/image_initial_065.png)  

<div class="alert alert-info memo">【Memo】発行頻度が指定されない場合は，［unknown］が設定されます。</div>

5-8 その他の機能 {#section5-8}
------------------------------

Enjuでは形態の設定として，その他，次の機能を利用できます。

### 5-8-1 国と地域を作成する {#section5-8-1}

* ［図書館の管理］メニューから［システムの設定］を選択します。
* ［国と地域］をクリックして，設定します。

{% include enju_setup/toc.md %}