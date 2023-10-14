---
title: ドキュメントを使用したインスタンスガバナンスガイドの作成
description: Marketo Engageインスタンスのドキュメントおよび変更ログを作成および管理するための堅牢な手順を確立する方法を説明します。 これにより、チームの知識共有にかかる時間を節約できるだけでなく、インスタンスの正常性と効率性を高めることができます。
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-12T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: true
source-git-commit: e7fe8da128a1c46620484d9b92823ba51791a671
workflow-type: tm+mt
source-wordcount: '906'
ht-degree: 1%

---


# ドキュメントを使用したインスタンスガバナンスガイドの作成

レガシー [!DNL Marketo Engage] 例えば、最新の機能および技術ドキュメントが不足しているという課題が多く発生します。 管理者として、適切なインスタンスガバナンスを確実におこなうためのガイドラインを確立することは、見落とすことのできない中核的な責任です。 ～するのは重要な戦略の一つだ [確立されたMarketo Engage・インスタンスで作業する際の効率の向上](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582).

このステップバイステップのチュートリアルは、 [!DNL Adobe Marketo Champion]Nick Hajdin は、このプロセスを通じて、インスタンスの設定の概要を説明し、主なオペレーショナル・プログラムを文書化し、 [!DNL changelog] 厳格なガバナンスポリシーを実施する。

## 継承されたインスタンスに対して、インスタンスガバナンスガイドとドキュメントを作成するのはなぜですか？

詳細なドキュメントと [!DNL changelog] は、お客様の内部での効率的な管理と知識の伝達に不可欠です。 [!DNL Marketo Engage] インスタンス。 インスタンスの設定時におこなった変更や決定を追跡すると、次の場合に役立ちます。

1. 拡張性の高い方法で、内部ユーザーをより簡単にトレーニングします。
2. でより効率的にビルド [!DNL Marketo Engage] 長期的には
3. インスタンスの健康と衛生状態を維持し、メールを調べる時間を節約します。 [監査記録](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html)、および [アクティビティログ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) コンテキストを取得するには
4. 転送時の時間を節約 [!DNL Marketo Engage] 新しい知識 [!DNL Marketo Engage] チームが売り上げを経験した場合は管理者。

## [!DNL Marketo Engage] ガバナンスガイド 101

ガバナンスガイドは、インスタンス設定とシステム設計の要件の真実の源となります。 このドキュメントに含めることをお勧めする主な情報は次のとおりです。

* プログラム/フォルダー構造
* ユーザーと役割の権限
* 通信制限
* ガバナンス基準
* プラットフォームへのアクセスを許可する前の内部ユーザートレーニング

## ガバナンスガイドを開発および維持する方法 [!DNL Marketo Engage] インスタンス

### 手順 1：ガバナンスガイドとドキュメントの現在の状態を特定する

* **継承されたインスタンスのドキュメントが見つかりません。** 最近新しい役割を開始したが、継承されたインスタンスのドキュメントが見つからない場合、 **手順 2 に進みます。** また、提供したダウンロード可能なテンプレートを使用して開始します。
* **ファイルに関するドキュメントを持っています。** おめでとう、これは良いサインです！ 関連性を確認し、最後の変更がいつおこなわれるかを確認します。 チームメンバーが積極的にメンテナンスしていない場合は、更新し、最新の状態に保つ方法について社内ユーザーに教え込むことをお勧めします。

### 手順 2：に含める要素を特定する [!DNL Marketo Engage] ドキュメントと [!DNL Changelogs]

形式は、クラウドベースのプラットフォームによって共有ドキュメントによって異なります。 組織のニーズに応じた形式をデザインできます。 [以下に、簡単なドキュメントと変更ログの Excel テンプレートを示します。](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) 最初に取り上げる重要な要素について説明します。 これには次が含まれます。

* ドキュメント
   * プログラムテンプレート名
   * チャネル
   * 作成日
   * 作成者
   * プログラムの目的
   * ステータス
   * プログラムテンプレートへのリンク
   * メモ
* Changelog
   * プログラムテンプレート名
   * 変更日
   * 更新者
   * 更新の目的
   * 変更前のエクスペリエンス（リンク/スクリーンショットを含む）
   * 変更後のエクスペリエンス（リンク/スクリーンショットを含む）
   * プログラムの URL

### ステップ 3：主なオペレーショナルプログラムの現在の状態を特定し、文書化する

最初に、サブスクリプションレベルでの影響を持つ主要なオペレーショナル・プログラムを特定します。 例としては、データ管理キャンペーン、リードのライフサイクル、リードスコアリング、 [!DNL CRM] 同期、配信品質。

特定された各オペレーショナルプログラムに対して、現在の状態を文書化します。 これには、プログラムの目的、設定、関連するスマートキャンペーン、他のツールとの統合（該当する場合）に関する詳細が含まれます。

### 手順 4：適用 [!DNL Changelog] メンテナンス

次のステップは、お客様の厳しいガバナンスポリシーを確立することです [!DNL Marketo Engage] &quot;を義務付けるインスタンス[!DNL Changelog] メンテナンス」 このポリシーでは、インスタンス全体のオペレーショナルプログラムに対しておこなわれた更新が、完全にドキュメント化されます。

これらのドキュメントの重要性と、それらに正しくアクセスして更新する方法について、チームに教えてください。 変更ログの管理に関する責任を割り当てると役立つ場合があります。そのため、指定されたマーケティングオペレーションチームの一部のメンバーや管理者は、変更を記録し、サインオフを提供し続けます。

### 手順 5：ドキュメントを一元化

お客様の [!DNL Marketo Engage] インスタンス。 共有ドライブ、専用フォルダ、クラウドベースのシステムなどが考えられます。

### 手順 6：定期的なレビューと更新

ドキュメントの定期的なレビューをスケジュールし、正確で最新の状態に保つようにします。 忙しい時には簡単に見落とすことができます。 予定表に事前にリマインダーを設定して、チームが定期的に更新を行い、オペレーショナルプログラムに変更や最適化を反映させるようにします。

## 次の手順

ダウンロードを開始する [単純テンプレート](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx).

上記の手順に従って、ガバナンスガイドとドキュメントを作成します。 このプロセスを進める際は、次の経験則に留意してください。

**既存のドキュメントを更新します。**
ドキュメントを最新の状態に保つことが非常に重要です。 過去 3 年間変更されていない場合は、インスタンスの監査時にドキュメントを改訂するように時間を割いてください。

**共有とトレーニング：**
ドキュメントを共有し、 [!DNL changelog] 関連するチームメンバーと共に、これらのレコードの更新方法に関する情報を提供します。

**定期的なレビュー：** 年間を通じてレビューとメンテナンスを行う時間を予め設定し、発生した新しい変更、最適化または調整を含めます。

Marketo Engageインスタンスに関する包括的で最新のドキュメントを保持することで、長期間の時間と労力を節約し、効果的なインスタンス管理を容易にします。

### 発言者

**ニック・ハジン**
[!DNL Adobe Marketo Champion] (2018)
*[!DNL Digital Technology Senior Manager at Accenture]*

![ニック・ハジン](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**エイミーチウ**
*導入とリテンションマーケティングマネージャ、Adobe*

![エイミーチウ](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width=30%}
