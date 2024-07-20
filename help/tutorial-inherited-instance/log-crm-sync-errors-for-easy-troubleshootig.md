---
title: CRM 同期エラーをログに記録して、トラブルシューティングを容易にする
description: CRM 同期エラーのログを使用して、CRM 同期の問題を調査し、スムーズに実行する方法を説明します。
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00Z
jira: KT-13875
thumbnail: KT-13875.jpeg
hide: false
exl-id: 3b7e6127-28fd-4dce-915d-5af9bcce984b
source-git-commit: 681d390ce5ab336a7e24cc63256659a492288517
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# CRM 同期エラーをログに記録して、トラブルシューティングを容易にする

Marketo Engage管理者は、インスタンスが CRM と同期しているかどうかを確認することが [ 毎日のルーチン ](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"} の重要な部分になるはずです。 [ 通知 ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} セクション（Marketo Engageインターフェイスの右上隅にあります）では頻繁な同期の問題を見つけて調査しますが、インスタンスのヘルスを組織的に管理するのに役立つヒントが用意されています。 AdobeのMarketo チャンピオン（2019～2022）、Amy Goldfine は、トラブルシューティングを容易にするために、管理者ユーザーに CRM 同期エラーのログを保持することをお勧めします。

![ 「同期エラー」タブのスクリーンショット ](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## CRM 同期エラーを記録するのはなぜですか？

Marketo Engage管理者は、CRM 同期エラーをログに記録することで、CRM 管理者と問題やトレンドをレビューし、根本原因を修正することができます。 次の手順に従って、インスタンスの CRM 同期の問題を文書化します。

## CRM 同期エラーのログを保持する方法

開始する前に、[CRM 同期エラーログテンプレート ](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx) をダウンロードしてください。

**手順 1:** Marketo Engageの *[!UICONTROL 管理者 ] セクション* に移動します。 *[!UICONTROL 統合]* の下で、使用する [!DNL CRM] に応じて「*[!DNL Salesforce]*」、「*[!DNL Microsoft Dynamics]*」、または「*[!DNL Veeva]*」をクリックし、「*[!UICONTROL 同期エラー]*」タブをクリックします。

**手順 2:** [ フィルター ] パネルを使用して、エラーのレコードを  [!DNL CSV]  ファイルとしてエクスポート [!UICONTROL  することを選択できます ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}。 数時間しかない場合は、「同期エラー *[!UICONTROL タブから直接コピーして貼り付け]* 方法をお勧めします。

**手順 3:** エラーが発生した日付をメモします。

**手順 4:** このエラーの影響を受ける人物レコードの数を入力します。 （CRM で 1 人のユーザーに対してのみエラーがスローされる場合があります。 同じエラーを一度に抱える人が多い場合があります）。

**手順 5:** エラーの影響を受けた 1 人の人物のメールアドレスをメモします。 これにより、エラーを簡単に参照して CRM 管理者と話し合うことができます。

**手順 6:** [!DNL Marketo Engage] 内の人物レコードへのリンクを貼り付け、その人物の [!UICONTROL CRM リード/連絡先 ] レコードを貼り付けます。

**手順 7:** 最後の列に、エラーの実際のテキストを貼り付けます。

## 次の手順

**エラーコードの特定：** エラーコードを理解するには、開発者向けドキュメント [ 応答レベルのエラーコードの表 ](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"} の説明を調べ、エラーを解決するための一般的な次の手順を見つけます。

## 作成者

**エイミー・ゴールドファイン**\
AdobeMarketoチャンピオン（2019 年～2022 年）
*創業者、MarketingOpsAdvice.com*

![ エイミー・ゴールドファイン ](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**エイミー・チウ**
*Adobe時の導入およびリテンションのマーケティングマネージャー*

![ エイミー・チウ ](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
