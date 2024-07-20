---
title: ドキュメントを含んだインスタンスガバナンスガイドの開発
description: Marketo Engageインスタンスのドキュメントと変更ログを作成および管理するための堅牢な手順を確立する方法を説明します。 これにより、チームの知識の共有に要する時間が節約されるだけでなく、インスタンスの正常性と効率も向上します。
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-14103
thumbnail: KT-14103.jpeg
hide: false
exl-id: 4313b54a-1848-4684-b037-7a7795dd01ec
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 1%

---

# ドキュメントを含んだインスタンスガバナンスガイドの開発

従来の [!DNL Marketo Engage] インスタンスに足を踏み入れると、多くの場合、最新の機能ドキュメントや技術ドキュメントを欠くという課題が生じます。 管理者として、適切なインスタンスガバナンスを確保するためのガイドラインを確立することは、見過ごすことができない中核的な責任です。 これは、[ 確立されたMarketo Engageインスタンスで作業する際の効率を高める ](https://nation.marketo.com/t5/champion-program-blogs/3-tips-to-increase-your-efficiency-in-an-inherited-instance/ba-p/247582) ための重要な戦略の 1 つです。

[!DNL Adobe Marketo Champion] （2018）の Nick Hajdin をソースとするこのステップバイステップのチュートリアルでは、このプロセスを通じて、インスタンス設定の概要を説明し、主要な運用プログラムを文書化し、厳密なガバナンスポリシーを適用するための [!DNL changelog] を維持します。

## 継承されたインスタンスにインスタンスガバナンスガイドおよびドキュメントを開発する理由

[!DNL Marketo Engage] インスタンス内での効率的な管理と知識の転送には、詳細なドキュメントと [!DNL changelog] が不可欠です。 インスタンスの設定中に行った変更や決定を追跡すると、次の利点があります。

1. スケーラブルな方法で、社内ユーザーのトレーニングを容易に実施できます。
2. 長期的には、[!DNL Marketo Engage] 内でより効率的に構築します。
3. コンテキストを取得するためのメール、[ 監査記録 ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/administration/audit-trail/audit-trail-overview.html)、[ アクティビティログ ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/smart-lists-and-static-lists/managing-people-in-smart-lists/locate-the-activity-log-for-a-person.html) の掘り下げに費やす時間を節約するために、インスタンスの正常性と衛生状態を今後も維持します。
4. チームで離職経験が [!DNL Marketo Engage] る場合に、新しい [!DNL Marketo Engage] 管理者に知識を転送する時間を節約できます。

## [!DNL Marketo Engage] ガバナンスガイド 101

ガバナンスガイドは、インスタンス設定およびシステム設計要件の情報源として機能します。 このドキュメントに含めることをお勧めする主な情報は次のとおりです。

* プログラム/フォルダー構造
* ユーザーと役割の権限
* 通信の制限
* ガバナンス基準
* プラットフォームへのアクセス権を付与する前に行う社内ユーザーのトレーニング

## [!DNL Marketo Engage] インスタンスのガバナンスガイドを開発および維持管理する方法

### 手順 1：現在のガバナンスガイドとドキュメントの状態を特定する

* **継承されたインスタンスのドキュメントが見つかりません：** 最近新しい役割を開始し、継承されたインスタンスのドキュメントが見つからない場合は、**手順 2 に進む** と、提供されたダウンロード可能なテンプレートの使用を開始します。
* **ファイルに関するドキュメントがあります：** おめでとうございます、これは良い兆候です！ 最後の変更が行われている時期を確認するには、それらの関連度を確認してください。 チームメンバーが積極的にメンテナンスしていない場合は、チームメンバーを更新し、内部ユーザーに対して最新のメンテナンス方法を教えることをお勧めします。

### 手順 2:[!DNL Marketo Engage] のドキュメントおよび [!DNL Changelogs] キュメントに含める要素を特定する

形式は、クラウドベースのプラットフォームから共有ドキュメントまで様々です。 組織のニーズに合わせて形式をデザインできます。 [ 簡単なドキュメントと変更ログの Excel テンプレート ](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) から始めることができる重要な要素を説明しています。 これには以下が含まれます。

* ドキュメント
   * プログラムテンプレート名
   * チャネル
   * 作成日
   * 作成者
   * プログラムの目的
   * ステータス
   * プログラムテンプレートへのリンク
   * メモ
* 変更ログ
   * プログラムテンプレート名
   * 変更日
   * 更新者
   * 更新の目的
   * 変更前のエクスペリエンス（リンク/スクリーンショットを含む）
   * 変更後のエクスペリエンス（リンク/スクリーンショットを含む）
   * プログラムへの URL

### 手順 3：主要な運用プログラムの現在の状態を特定して文書化する

まず、サブスクリプションレベルで影響を受ける主要な運用プログラムを特定します。 例としては、データ管理キャンペーン、リードライフサイクル、リードスコアリング、リード同期、配信品 [!DNL CRM] が挙げられます。

特定された運用プログラムごとに、その現在の状態をドキュメント化します。 これには、プログラムの目的、設定、関連するスマートキャンペーンおよび他のツールとの統合（該当する場合）に関する詳細が含まれます。

### 手順 4:[!DNL Changelog] メンテナンスの適用

次の手順では、「[!DNL Changelog] スタムメンテナンス」を義務付ける [!DNL Marketo Engage] インスタンスの厳密なガバナンスポリシーを確立します。 このポリシーにより、インスタンス全体で運用プログラムに対して行われた更新が完全にドキュメント化されます。

これらのドキュメントの重要性と、ドキュメントに適切にアクセスして更新する方法について、チームを教育します。 変更ログを維持する責任を割り当てると便利です。そのため、少数の専任のマーケティング運用チームメンバーまたは管理者が、変更を継続的に記録し、承認を提供します。

### 手順 5：ドキュメントを一元化

[!DNL Marketo Engage] インスタンスに関連するすべてのドキュメントを保存するための一元的な場所またはリポジトリを確立します。 これは、共有ドライブ、専用フォルダー、クラウドベースのシステムのいずれかです。

### 手順 6：定期的なレビューと更新

ドキュメントを正確かつ最新の状態に保つために、ドキュメントの定期的なレビューをスケジュールします。 それは忙しい時間の間に簡単に見過ごすことができます。 プロアクティブにカレンダーにリマインダーを設定して、運用プログラムの変更や最適化を反映するためにチームが定期的に更新を行うようにします。

## 次の手順

この [ シンプルなテンプレート ](/help/tutorial-inherited-instance/_assets/downloads/Adobe_Marketo_Engage_Inherited_Instance_Documentation-Changlog.xlsx) をダウンロードして開始します。

上記の手順に従って、ガバナンスガイドとドキュメントを作成します。 プロセスを進める際は、次の経験則に留意してください。

**既存のドキュメントを更新する：**
ドキュメントを最新の状態に保つことが重要です。 過去 3 年間変更されていない場合は、インスタンスを監査する際にドキュメントを修正する時間を確保します。

**共有とトレーニング：**
関連するチームメンバーとドキュメントや [!DNL changelog] ールを共有し、これらのレコードを更新する方法を学びます。

**定期的レビュー：** 新しい変更、最適化、調整が発生した場合にそれを含めるために、1 年を通じてレビューおよび維持する事前スケジュール時間。

Marketo Engageインスタンスの包括的な最新ドキュメントを保持することで、長期的に時間と労力を節約し、効果的なインスタンス管理を容易にすることができます。

### 作成者

**ニック・ハジン**
[!DNL Adobe Marketo Champion] （2018）
*[!DNL Digital Technology Senior Manager at Accenture]*

![ ニック・ハジン ](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Nicholas_Hajdin.png){width="30%"}

**エイミー・チウ**
*Adobe、Adoption &amp; Retention Marketing Manager*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){ 幅=30%}
