---
title: 簡単なトラブルシューティング用のCRM同期エラーのログ
description: CRM同期エラーのログを使用して、CRM同期の問題を調査し、円滑に実行する方法を説明します。
feature: Administration
role: Admin
level: Intermediate, Experienced
doc-type: Tutorial
last-substantial-update: 2023-10-16T00:00:00.000Z
jira: KT-13875
thumbnail: KT-13875.jpeg
index: true
exl-id: 3b7e6127-28fd-4dce-915d-5af9bcce984b
TQID: https://experienceleague.adobe.com/JM26ZReC9P8rKS8IqjIV5TKLxT0xInUHysdM7zo0LzM
product_v2: id: b27e5950-9033-45ac-9f86-eb22e567f615
feature_v2: id: d1d0a9cd-295d-4976-8c39-ddae266f240e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0f8ea3988fd586ccbd4b414b3558f6e5f36882bf
workflow-type: tm+mt
source-wordcount: 470
ht-degree: 1%

---

# 簡単なトラブルシューティング用のCRM同期エラーのログ

Marketo Engage管理者は、インスタンスがCRMと同期しているかどうかを確認することが、[毎日のルーチン ](https://nation.marketo.com/t5/champion-program-blogs/my-marketo-morning-routine-tips-for-driving-marketing-operation/ba-p/247508){target="_blank"}の重要な部分である必要があります。 [通知セクション ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/core-marketo-concepts/miscellaneous/notification-types.html){target="_blank"} （Marketo Engage インターフェイスの右上隅にあります）では、頻繁な同期の問題を確認して調査できますが、インスタンスの正常性を整理して管理するのに役立つプロ向けのヒントがあります。 Adobe Marketo Champion （2019～2022）、Amy Goldfineは、管理者ユーザーがCRM Sync エラーのログを保持して、トラブルシューティングを容易にすることをお勧めします。

![同期エラーのタブのスクリーンショット ](/help/tutorial-inherited-instance/_assets/Marketo_Engage_Admin_Salesforce_Sync_Errors_Tab.png)

## CRM同期エラーの記録を保持する理由

CRM Sync エラーをログに記録することで、Marketo Engage管理者はCRM管理者の問題と傾向を確認して、根本原因を修正できます。 以下の手順に従って、インスタンスのCRM同期の問題を文書化します。

## CRM同期エラーのログを保持する方法

開始する前に、[CRM Sync Errors Log テンプレート ](/help/tutorial-inherited-instance/_assets/downloads/Adobe-Marketo-Engage_CRM-Sync-Error-Log-Template.xlsx)をダウンロードしてください。

**手順1:** Marketo Engageの&#x200B;*[!UICONTROL 管理者] セクション*&#x200B;に移動します。 *[!UICONTROL 統合]*&#x200B;で、使用している[!DNL CRM]に応じて&#x200B;*[!DNL Salesforce]*、*[!DNL Microsoft Dynamics]*&#x200B;または&#x200B;*[!DNL Veeva]*&#x200B;をクリックし、「*[!UICONTROL 同期エラー]*」タブをクリックします。

**手順2:** [!UICONTROL  フィルター] パネル ](https://experienceleague.adobe.com/docs/marketo/using/product-docs/crm-sync/salesforce-sync/salesforce-sync-errors.html#filter-sync-errors){target="_blank"}を使用して、エラーの記録を [!DNL CSV]  ファイルとして[書き出すことを選択できます。 時間が数時間しかない場合、「*[!UICONTROL 同期エラー]*」タブから直接コピー&amp;ペーストすることをお勧めします。

**手順3:** エラーが発生した日付を記録します。

**手順4:**&#x200B;そのエラーの影響を受ける人物レコードの数を入力します。 （CRMでエラーがスローされるのは、1人の場合だけです。 同じエラーを一度に持つ人が多い場合があります。

**手順5:** エラーの影響を受ける1人のユーザーの電子メールアドレスをメモします。 これにより、CRM管理者がエラーを参照して議論することが容易になります。

**手順6:**&#x200B;その人物の[!DNL Marketo Engage]および[!UICONTROL CRM リード/コンタクト ] レコードの人物レコードにリンクを貼り付けます。

**手順7:**&#x200B;最後の列に、エラーの実際のテキストを貼り付けます。

## 次のステップ？

**エラーコードの特定：** エラーコードを理解するには、開発者ドキュメント [応答レベルのエラーコード テーブル ](https://developers.marketo.com/rest-api/error-codes/#response_level_error_codes){target="_blank"}の説明を参照し、エラーを解決するための一般的な次の手順を見つけます。

## 制作者

**Amy Goldfine**\
Marketoチャンピオン（2019-2022）
*Founder, MarketingOpsAdvice.com*

![Amy Goldfine](/help/tutorial-inherited-instance/_assets/authors/Customer_Author_Amy_Goldfine.png){width="25%"}

**Amy Chiu**
*Adobeの導入および維持マーケティングマネージャー*

![Amy Chiu](/help/tutorial-inherited-instance/_assets/authors/Adobe_Author_Amy_Chiu.png){width="25%"}
