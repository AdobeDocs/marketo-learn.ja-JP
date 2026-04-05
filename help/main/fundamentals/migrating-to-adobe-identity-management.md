---
title: Adobe Identity Management への移行
description: このチュートリアルは、Marketo Engage サブスクリプションとユーザの Adobe Admin Console への移行を進める際に役立ちます。
role: Admin
level: Intermediate, Experienced
recommendations: noDisplay, noCatalog
last-substantial-update: 2024-07-26T00:00:00Z
feature: Marketing
exl-id: 8368a148-c0c8-462f-b166-9efc412c4a0f
source-git-commit: 096d4b42008446a72f92b8fe509c0c216bc8f904
workflow-type: tm+mt
source-wordcount: '1428'
ht-degree: 93%

---

# Adobe Identity Management への移行

アドビは、Adobe Marketo Engage サブスクリプションとユーザの管理方法を強化しています。 Marketo Engage サブスクリプションとユーザを Adobe Admin Console に移行することで、組織の生産性が向上します。

このチュートリアルは、管理者が、ユーザの他のアドビアカウントや製品とともに、Adobe Marketo Engage の一元的な管理を開始できるよう、移行をお手伝いします。 移行は必須であり、マーケティングワークフロー、コンテンツ、統合、アセットには影響しません。

## Marketo Engage 管理者向け移行前チェックリスト {#pre-migration-checklist-for-marketo-engage-administrators}

組織が Adobe Marketo Engage を Adobe Admin Console に移行できるようにするには、以下のチェックリストに従って今後の変更を管理することをお勧めします。

### &#x200B;1. システム管理者とIT チームを特定し、必要なアクションについて話し合います {#identify-your-system-administrators}

* 組織内のシステム管理者が誰であるかわからない場合は、アドビのアカウントチームまたはアドビサポート `marketocares@marketo.com` にお問い合わせください。

* Marketo Engage サブスクリプションの移行先となる Adobe Admin Console（またはAdobe 組織）を確認します。 Marketo Engage のネイティブ対話自動処理ツールである [Dynamic Chat](/help/main/dynamic-chat/dynamic-chat-overview.md){target="_blank"} 用の Adobe Admin Console を使用している方も多いでしょう。 Marketo Engage サブスクリプションは、Dynamic Chat と同じ組織にデプロイする必要があります。

* Adobe ID への移行後に Marketo Engage へのアクセスが中断されないようにするには、IT チームと協力して、[この記事の上部](https://experienceleague.adobe.com/ja/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}に記載されているすべての Adobe ドメインを許可リストに登録します。

* **オプション：**&#x200B;ユーザ移行の前に[シングルサインオン（SSO）を実装](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console#subscription-migration-complete){target="_blank"}します。

  >[!NOTE]
  >
  >Marketo Engage でサポートされる SSO と Adobe Admin Console SSO には違いがあります。 そのため、設定の変更を実装する必要がある場合があります。

* **オプション：** Marketo Engage ユーザの認証状態が維持されたままになるように、ユーザ移行の前に[目的の最大セッション有効期間](https://helpx.adobe.com/jp/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"}をカスタマイズします。

* システム管理者との通信内容について詳しくは、[サンプルメールの節](#announce-the-migration-timeline)を参照してください。

### &#x200B;2. Adobe Identityへの移行の変更点と影響について説明します {#familiarize-yourself-with-the-changes}

次のビデオでは、Marketo Engage 製品管理チームが移行ジャーニーと期待される結果について説明します。

>[!VIDEO](https://video.tv.adobe.com/v/3430920t3/?t=170/?quality=12&learn=on){transcript=true}

Marketo Engage 管理者向けのこのトピックに関するヘルプについて詳しくは、次のヘルプ記事を参照してください。

* [ユーザー設定チェックリスト](https://experienceleague.adobe.com/ja/docs/marketo/using/getting-started/initial-setup/user-setup){target="_blank"}

* [Adobe Identity Management の概要](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/adobe-identity-management-overview){target="_blank"}

* [Marketo サブスクリプションと Adobe Admin Console へのユーザーの移行について](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/understanding-marketo-subscription-and-user-migration-to-the-adobe-admin-console){target="_blank"}

* [Migration Consoleを使用したAdobe IDへの移行](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity){target="_blank"}

* [Adobe Admin Consoleの使用方法を理解する](https://helpx.adobe.com/jp/enterprise/using/admin-console.html){target="_blank"}

### &#x200B;3. 社内チームに必要な移行のスケジュールと準備を発表する {#announce-the-migration-timeline}

* Marketo Engage 管理者とユーザのカレンダーに、スケジュールに従って移行日をマークします。

   * 内部タイムラインに合わせて、**管理**／**移行コンソール**／**移行前**&#x200B;で移行日を変更できます。 再スケジュールと制限事項について詳しくは、[移行日の変更](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/marketo-with-adobe-identity/subscription-and-user-migration/migrating-to-adobe-identity#pre-migration){target="_blank"}を参照してください。

* **システム管理者へのメールの送信**

管理者に送信するサンプルメールを以下に示します。 通常、IT 部門がすべての Adobe ライセンスを管理します。

+++ システム管理者に送信するサンプルメール

**件名：サポートが必要 - Adobe Admin Console への Marketo Engage サブスクリプションの移行**

`[IT Administrator/NAME]` 様

Marketo Engage サブスクリプションは、間もなく Adobe Identity Management System に移行されます。 Marketo Engage ユーザへの影響を最小限に抑えるために、`[Marketing Operation team]` では、ユーザの移行開始前に必要な手順を完了していただく必要があります。ご協力をお願いいたします。

`1.` 組織が既に Adobe Admin Console で他のアドビ製品を管理しているかどうか、Marketo Engage を同じコンソールに移行するかどうかを確認します。

* Marketo Engage サブスクリプションは、Marketo Engage に統合されたネイティブの対話自動処理ツールである Dynamic Chat と同じ組織にある必要があります。

* Admin Console に関するご質問やご不明な点がございましたら、アドビサポート（`marketocares@marketo.com`）にお問い合わせください。CC に含めて送信してください。

`2.` アドビから「Adobe Marketo Engage `[Package Tier]` へのユーザアクセス管理に必要なアクション」という件名のメールが届きますので、確認します。 このメールは、Admin Console で Marketo Engage ライセンスがプロビジョニングされた後に送信されました。 このメールはシステム管理者にのみ送信されます。 受信されましたら、速やかにご連絡ください。

* アドビは、Admin Console のシステム管理者であるお客様に、ユーザを組織の既存のコンソールへと自動的に移行する同意を求める場合があります。 「Adobe Marketo Engage `[Package Tier]` へのユーザアクセス管理に必要なアクション」という件名のメールに記載されている「開始」ボタンをクリックして、同意ページに移動します。

`3.` 移行後、Marketo Engage は experience.adobe.com から Adobe Experience Cloud に提供されるようになります。 Marketo Engage へのアクセスが中断されないようにするには、[この記事の上部](https://experienceleague.adobe.com/ja/docs/marketo/using/getting-started/initial-setup/configure-protocols-for-marketo){target="_blank"}に記載されているすべての Adobe ドメインを許可リストに登録してください。

`4.` **オプション：** Adobe Admin Console で SSO（シングルサインオン）を設定します。

* 今後、Adobe ID で SSO でログインするユーザにメリットを与えるには、ユーザ移行前に Adobe Admin Console で SSO の設定をお願いいたします。

`5.` **オプション：** Adobe Admin Console で[最大セッション有効期間](https://helpx.adobe.com/jp/enterprise/using/authentication-settings.html#advanced-settings){target="_blank"}を長く設定します。

* ユーザが頻繁にログインする必要がないように、セッション有効期間を長く設定して詳細設定でカスタマイズしてください。

移行期間中のご協力に感謝いたします。 これらの手順を完了したらお知らせください。移行作業を進めさせていただきます。

よろしくお願いします。

`[Your Name]`

+++

* **Marketo Engage ユーザーへのメールの送信**

管理者権限を持た&#x200B;**ない** Marketo Engage ユーザ向けのサンプルメールを以下に示します。

+++ 今後の移行を通知するサンプルメール

**件名：重要な更新 - Adobe Admin Console への Marketo Engage サブスクリプションの移行**

Marketo Engage ユーザの皆様

Marketo Engage インスタンスとログイン方法に関する重要なお知らせがあります。 アドビでは、Marketo Engage サブスクリプションとユーザを Adobe Admin Console に移行しています。これにより、すべての製品管理を一元化できます。 これは、マーケティングワークフロー、コンテンツ、統合、アセットには影響しません。

**主な詳細：**

* **移行日**：`[Specify the scheduled date - please find this in Marketo Engage under Admin > Migration Console > Pre-migration]`

* **タイミング**：移行は、サブスクリプションの現地時間の午前 0 時頃に開始されます。

* **影響**：ユーザの移行中に、製品へのアクセスが失われることはありません。 アカウントの移行時にログインしている場合は、ログアウトされ、移行後、Adobe ID を使用して数分以内に再度ログインするように促されます。

* **メリット**：Adobe ID または Adobe Federated ID（SSO）のいずれかの単一の Adobe ID を使用して、Marketo Engage と他のアドビ製品を認証できます。

**必要な作業：**

`1.` **準備**：Adobe ID に移行するには、メールの確認が必要です。

私は。 リンク付きの電子メール確認リクエスト電子メールを受信しました（3日間有効です）。 リンクの有効期限が切れている場合は、Marketo Engage 内から「マイプロファイル」アイコンをクリックして、**マイアカウント**／**アカウント設定**／**確認を再送信**&#x200B;に移動すると、確認メールを再送信できます。

ii. メール確認を成功させるには、アクティブなユーザセッションが必要です。 まず、ID プロバイダー（IdP）の URL を使用して Marketo Engage サブスクリプションにログインしてください。

`2.` **オンボード**：ユーザアカウントが移行されると、アドビからログイン方法の変更に関するメールが届きます。

私は。 「招待を承諾」ボタンをクリックし、Adobe IDを使用してログインすると、新しい招待を承諾できます。

ii. アドビのログインページで、既存の Adobe ID を使用してログインします。

iii. 移動先の engage-xx.marketo.com ドメインで以前にブックマークした URL がある場合は、まず Marketo Engage インスタンスにログインする必要があります。

`3.` **お問い合わせ**：アカウントの移行後にご質問やサポートが必要な場合や、アカウントが移行されずに Marketo Engage へのアクセスが失われてしまった場合は、`[your internal contact email/phone]` の Marketo Engage 移行チームにお問い合わせください。

移行期間中のご協力に感謝いたします。 システムのセキュリティを維持するためのご理解とご協力をお願いいたします。

よろしくお願いします。

`[Your Name]`

+++
