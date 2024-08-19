---
title: AdobeIdentity Managementへの移行
description: このチュートリアルは、Marketo EngageのサブスクリプションとユーザーのAdobe Admin Consoleへの移行方法を説明します。
role: User
level: Beginner
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: 4ecbe3a79ad28a38e3c630868663a7b2859428e9
workflow-type: tm+mt
source-wordcount: '1170'
ht-degree: 0%

---

# AdobeIdentity Managementへの移行

Adobeは、Adobe Marketo Engageのサブスクリプションとユーザーの管理方法を強化しています。 Marketo EngageのサブスクリプションとユーザーをAdobe Admin Consoleに移行することで、お客様の組織の生産性を向上させます。

このチュートリアルは移行手順を支援し、ユーザー用の他のAdobeアカウントおよび製品と共にAdobe Marketo Engageの管理を一元的に開始できるようにします。 移行は必要であり、マーケティングワークフロー、コンテンツ、統合またはアセットには影響しません。

## Marketo Engage管理者向けの移行前チェックリスト {#pre-migration-checklist-for-marketo-engage-administrators}

Adobe Marketo EngageをAdobe Admin Consoleに移行できるようにするには、以下のチェックリストに従って、今後の変更内容を管理することをお勧めします。

### 1. システム管理者と IT チームを特定し、必要なアクションについて話し合います {#identify-your-system-administrators}

* システム管理者が不明な場合は、Adobeアカウントチームに問い合わせるか、Adobeサポート `marketocares@marketo.com` ームにお問い合わせください。

* Marketo Engageのサブスクリプションを移行するAdobe Admin Console（またはAdobe組織）を指定します。 Marketo Engageのネイティブ会話自動処理ツールである ](/help/dynamic-chat/dynamic-chat-overview.md){target="_blank"}0}Dynamic Chat} のAdobe Admin Consoleがある可能性があります。 [Marketo Engageサブスクリプションは、Dynamic Chatと同じ組織にデプロイする必要があります。

* IT チームと協力して、[ この記事の上部 ](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} に一覧表示されているすべてのAdobeドメインを許可リストに加えるし、Adobe ID への移行後にMarketo Engageアクセスが中断されるのを防ぎます。

* **オプション：**[ シングルサインオン（SSO）を実装 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"} ユーザー移行前。

* システム管理者との通信方法については、[ サンプルメールの節 ](#announce-the-migration-timeline) を参照してください。

### 2. Adobe ID への移行による変化と影響を確認する {#familiarize-yourself-with-the-changes}

次のビデオでは、Marketo Engage製品管理チームが、移行ジャーニーと予想される結果について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?t=170/?quality=12&learn=on){transcript=true}

このトピックに関するMarketo Engage管理者向けのヘルプについては、次のヘルプ記事を参照してください。

* [ ユーザー設定チェックリスト ](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [AdobeIdentity Managementの概要 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Marketo サブスクリプションとAdobe Admin Consoleへのユーザー移行について ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [ 移行コンソールを使用したAdobe ID への移行 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Adobe Admin Consoleの使用方法について ](https://helpx.adobe.com/jp/enterprise/using/admin-console.html){target="_blank"}

### 3.社内チームに必要な移行タイムラインと準備を知らせる {#announce-the-migration-timeline}

* Marketo Engage管理者とユーザーのカレンダーに、スケジュールに従って移行日をマークします。

   * 内部タイムラインに合わせて、**管理者**/**移行コンソール**/**移行前** で移行日を変更できます。 再スケジュールと [ 移行日の変更 ](https://experienceleague.adobe.com/en/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"} の制限事項について詳しく説明します。

* **システム管理者へのメールの送信**

以下は、システム管理者に送信するメールのサンプルです。 通常、IT 部門は、すべてのAdobeライセンスを管理します。

`---------------------------------------------------`

**件名：サポートが必要 – Adobe Admin ConsoleへのMarketo Engageのサブスクリプションの移行**

Kaemayku`[IT Administrator/NAME]`、

Marketo Engageのサブスクリプションは、間もなくAdobeIdentity Managementシステムに移行されます。 `[Marketing Operation team]` は、Marketo Engageユーザーへの影響を最小限に抑えるために、ユーザーの移行開始前に必要な手順を完了するためにユーザーの支援を必要としています。

`1.` 組織が既にAdobe Admin Consoleで他のAdobeMarketo Engageを管理しているかどうか、また製品が同じコンソールに移行されるかどうかを確認します。

* Marketo Engageのサブスクリプションは、Marketo Engageと統合されたネイティブな会話自動処理ツールであるDynamic Chatと同じ組織に存在する必要があります。

* Admin Consoleに関するご質問やご不明な点については、Adobeサポート（`marketocares@marketo.com`）および CC までお問い合わせください。

`2.` 件名が「Adobe Marketo Engage `[Package Tier]` へのユーザーアクセスの管理に必要なアクション」である、Adobeからのメールを探してください。 このメールは、Admin ConsoleにMarketo Engageライセンスがプロビジョニングされた後に送信されました。 このメールはシステム管理者にのみ送信されます。 受け取り次第お知らせ下さい。

* Adobeは、Admin Consoleのシステム管理者であるお客様の同意を得て、ユーザーを当社の組織の既存のコンソールに自動的に移行する場合があります。 件名が「Adobe Marketo Engage `[Package Tier]` へのユーザーアクセスを管理するために必要なアクション」のメールで、「開始」ボタンをクリックして同意ページに移動します。

`3.` 移行後、Marketo Engageはexperience.adobe.comからAdobe Experience Cloudに提供されるようになります。 Marketo Engageへのアクセスが中断されないように、[ この記事の上部 ](https://experienceleague.adobe.com/en/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"} に記載されているすべてのAdobeドメインを許可リストに加えるしてください。

`4.` **オプション：** Adobe Admin Consoleでの SSO （シングルサインオン）の設定。

* 今後、Adobe ID で SSO でログインするユーザーの利益となるよう、ユーザーの移行が行われる前に、Adobe Admin Consoleで SSO の設定を支援してください。

今回の移行にご協力いただき、ありがとうございます。 これらの手順が完了したら連絡して、移行を続行します。

よろしくお願いします。

`[Your Name]`

`---------------------------------------------------`

* **Marketo Engageユーザーへのメールの送信**

以下は、管理者権限を持たないMarketo Engageユーザーに今後の移行を通知するために使用できるサンプルメールです。

`---------------------------------------------------`

**件名：重要な更新 – Adobe Admin ConsoleへのMarketo Engage購読の移行**

Marketo Engageユーザー各位

Marketo Engageインスタンスとログイン方法に関する重要なお知らせがあります。 Adobeでは、Marketo EngageのサブスクリプションとユーザーをAdobe Admin Consoleに移動しています。これにより、すべての製品管理を 1 か所で一元化できます。 これは、マーケティングワークフロー、コンテンツ、統合またはアセットには影響しません。

**キーの詳細：**

* **移行日**: `[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **タイミング**：移行は現地時間の午前 0 時頃に開始されます。

* **影響**：ユーザーの移行中に、製品へのアクセスが失われることはありません。 アカウントの移行中にログインすると、ログアウトされ、移行後にAdobe ID を使用して数分以内にログインし直すように求められます。

* **メリット**:Adobe IDまたはAdobeFederated ID（SSO）の 1 つのAdobe ID を使用して、Marketo Engage製品やその他のAdobe製品を認証します。

**必要な手順：**

`1.`**準備**:Adobe ID に移行するには、メール検証が必要です。

i. リンクが記載された確認のメールが届いています（3 日間有効です）。 リンクの有効期限が切れている場合は、「マイプロファイル」アイコンをクリックし、**マイアカウント**/**アカウント設定**/**再送信認証** に移動して、Marketo Engageから認証メールを再送信できます。

ii.電子メールの検証を成功させるには、アクティブなユーザーセッションが必要です。 最初に ID プロバイダー（IdP）の URL を使用して、Marketo Engageのサブスクリプションにログインしてください。

`2.` **オンボード**：ユーザーアカウントが移行されると、ログイン方法の変更に関するメールがAdobeから送信されます。

i. [ 招待の承諾 ] ボタンをクリックし、Adobe ID を使用してサインインすることで、新しい招待を承諾します。

ii.Adobeログインページで、既存のAdobe IDにログインしてください。

iii.移動先のengage-xx.marketo.com ドメインで以前にブックマークした URL のMarketo Engageインスタンスにまずログインする必要があります。

`3.` **お問い合わせ**: アカウントの移行後にご質問がある場合、またはサポートが必要な場合、またはアカウントが移行されておらずMarketo Engageへのアクセス権を失った場合は、`[your internal contact email/phone]` のMarketo Engage移行チームにお問い合わせください。

今回の移行にご協力いただき、ありがとうございます。 システムのセキュリティを維持するためのご理解とご協力をお願いいたします。

よろしくお願いします。

`[Your Name]`

`---------------------------------------------------`
