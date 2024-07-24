---
title: AdobeIdentity Managementへの移行
description: 説明を準備中です。
role: User
level: Beginner
hide: true
hidefromtoc: true
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: fe760c2fc53b96d5c176de377730bce2e89dbc74
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 0%

---

# AdobeIdentity Managementへの移行

Adobeは、Adobe Marketo Engageのサブスクリプションとユーザーの管理方法を強化しています。 Marketo EngageのサブスクリプションとユーザーをAdobe Admin Consoleに移行することで、お客様と組織の生産性を向上させます。

このチュートリアルでは移行手順を説明し、ユーザーの他のAdobeアカウントおよび商品と共にAdobe Marketo Engageを一元的に管理できるようにします。 移行は必要であり、マーケティングワークフロー、コンテンツ、統合またはアセットには影響しません。

## Marketo Engage管理者向けの移行前チェックリスト {#pre-migration-checklist-for-marketo-engage-administrators}

Adobe Marketo EngageをAdobe Admin Consoleに移行できるようにするには、以下のチェックリストに従って、今後の変更内容を管理することをお勧めします。

### 1. システム管理者を特定し、その管理者が実行する必要があるアクションについて話し合います {#identify-your-system-administrators}

* システム管理者が不明な場合は、Adobeアカウントチームに問い合わせるか、Adobeサポート `marketocares@marketo.com` ームにお問い合わせください。

* Marketo Engageのサブスクリプションを移行するAdobe Admin Console（またはAdobe組織）を指定します。  Marketo Engageのサブスクリプションは、Marketo Engageと統合されたネイティブな会話自動処理ツールであるDynamic Chatと同じ組織にデプロイする必要があります。
  `TBD LINK TO https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete`

* システム管理者との通信方法について詳しくは、[ サンプルメールの節 ](#announce-the-migration-timeline) を参照してください。

### 2. Adobe ID への移行による変化と影響を確認する {#familiarize-yourself-with-the-changes}

次のビデオでは、Marketo Engage製品管理チームが、移行ジャーニーと予想される結果について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?quality=12&learn=on){transcript=true}

このトピックに関するMarketo Engage管理者向けのヘルプについては、次のヘルプ記事を参照してください。

* [ ユーザー設定チェックリスト ](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [AdobeIdentity Managementの概要 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Marketo サブスクリプションとAdobe Admin Consoleへのユーザー移行について ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [ 移行コンソールを使用したAdobe ID への移行 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Adobe Admin Consoleの使用方法について ](https://helpx.adobe.com/jp/enterprise/using/admin-console.html){target="_blank"}

### 3.社内チームに必要な移行タイムラインと準備を知らせる {#announce-the-migration-timeline}

* Marketo Engage管理者とユーザーのカレンダーに、スケジュールに従って移行日をマークします。

**Admin**/**Migration Console**/**Pre-Migration** で移行日を変更して、内部タイムラインとの整合性を高めることができます。 再スケジュールと [ 移行日の変更 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"} の制限事項について詳しく説明します。

* システム管理者と通信するためのメールを送信します。

以下は、システム管理者に送信するメールのサンプルです。 通常、IT 部門は、すべてのAdobeライセンスを管理します。

`---------------------------------------------------`

**件名：サポートが必要 – Adobe Admin ConsoleへのMarketo Engageのサブスクリプションの移行**

Kaemayku`[IT Administrator/NAME]`、

Marketo Engageのサブスクリプションは、間もなくAdobeIdentity Managementシステムに移行されます。 `[Marketing Operation team]` は、Marketo Engageユーザーへの影響を最小限に抑えるために、ユーザーの移行開始前に必要な手順を完了するためにユーザーの支援を必要としています。

`1.` 組織が既にAdobe Admin Consoleで他のAdobeMarketo Engageを管理しているかどうか、また製品が同じコンソールに移行されるかどうかを確認します。

* Marketo Engageのサブスクリプションは、Marketo Engageと統合されたネイティブな会話自動処理ツールであるDynamic Chatと同じ組織にある必要があります。

* Marketo Engageが追加されるAdmin Consoleに関するご質問やご不明な点については、`marketocares@marketo.com` のサポートチームにお問い合わせください。

`2.` 件名が「Adobe Marketo Engage `[Package Tier]` へのユーザーアクセスの管理に必要なアクション」である、Adobeからのメールを探してください。 このメールは、Admin ConsoleにMarketo Engageライセンスがプロビジョニングされた後に送信されました。 このメールはシステム管理者にのみ送信されます。 受け取り次第お知らせ下さい。

* Adobeは、Admin Consoleのシステム管理者であるお客様の同意を得て、ユーザーを組織の既存のコンソールに自動移行する場合があります。 件名が「Adobe Marketo Engage `[Package Tier]` へのユーザーアクセスを管理するために必要なアクション」のメールで、「開始」ボタンをクリックして同意ページに移動します。

`3.` **オプション：** Adobe Admin Consoleでの SSO （シングルサインオン）の設定。

* 今後、ユーザー ID で SSO を使用してログインする際にメリットを得るために、Adobe移行が行われる前に、Adobe Admin Consoleでの SSO 設定に関するサポートをお願いします。
今回の移行にご協力いただき、ありがとうございます。 これらの手順が完了したら、お知らせください。そうすれば、Marketo Engageを使用してユーザーの移行を進めることができます。
よろしくお願いします。

`[Your Name]`

`---------------------------------------------------`

* Marketo Engageユーザーにメールを送信します。

以下は、管理者の権限を持たないMarketo Engageユーザーに今後の移行をお知らせするために使用できるサンプルメールです。

`---------------------------------------------------`

**件名：重要な更新 – Adobe Admin ConsoleへのMarketo Engage購読の移行**

Marketo Engageユーザー各位

Marketo Engageインスタンスとログイン方法に関する重要なお知らせがあります。 Adobeは、Marketo EngageのサブスクリプションとユーザーをAdobe Admin Consoleに移動して、顧客がすべての製品管理を 1 か所で一元化できるようにしています。 これは、マーケティングワークフロー、コンテンツ、統合またはアセットには影響しません。

主な詳細：

* 移行日：[ スケジュールされた日付を指定します。これを **管理者**/**移行コンソール**/**事前移行の下のMarketo Engageで確認してください**]

* タイミング：移行はサブスクリプションの現地時間の午前 0 時頃に開始されます。

* 影響：ユーザーの移行中に、製品へのアクセスが失われることはありません。 アカウントの移行中にログインすると、ログアウトされ、移行後にAdobe ID を使用して数分以内にログインし直すように求められます。

* メリット：Adobe IDまたはAdobeFederated ID（SSO）の 1 つのAdobeID を使用して、Marketo Engage製品やその他のAdobe製品を認証します。

必要な手順：

`1.` 準備：Adobe ID に移行するには、メールの検証が必要です。

i. リンクが記載された確認のメールが届いています（3 日間有効です）。 リンクの有効期限が切れている場合は、**管理者**/**マイアカウント**/**アカウント設定** に移動し、「検証を再送信 **をクリックして検証メールを再送信できます**。
ii.電子メールの検証を成功させるには、アクティブなユーザーセッションが必要です。 最初に ID プロバイダー（IdP）の URL を使用して、Marketo Engageのサブスクリプションにログインしてください。

`2.` Onboard: ユーザーアカウントが移行されると、ログイン方法の変更に関するメールがAdobeから送信されます。

i. [ 招待の承諾 ] ボタンをクリックし、Adobe ID を使用してサインインすることで、新しい招待を承諾します。
ii.Adobeログインページで、既存のAdobe IDにログインしてください。

`3.` お問い合わせ：アカウントの移行後にご質問がある場合、またはアカウントが移行されておらずMarketo Engageへのアクセス権を失った場合は、`[your internal contact email/phone]` のMarketo Engage移行チームにお問い合わせください。

今回の移行にご協力いただき、ありがとうございます。 システムのセキュリティを維持するためのご理解とご協力をお願いいたします。

最高の

`[Your Name]`

`---------------------------------------------------`
