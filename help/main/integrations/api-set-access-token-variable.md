---
title: Marketo APIの操作方法ビデオ – 変数にアクセストークンを設定する方法
description: Postman アプリケーションを設定する方法と、再利用性のために変数にデータを保存するために変数を活用する方法について説明します。
feature: REST API
role: Admin, Developer
level: Experienced
doc-type: Technical Video
duration: 772
last-substantial-update: 2024-08-06T00:00:00.000Z
jira: KT-15548
exl-id: 4da86ed6-1072-4e0e-a648-16587badaeb3
product_v2:
  - id: b27e5950-9033-45ac-9f86-eb22e567f615
    internal-label: Marketo Engage
feature_v2:
  - id: dca84292-69e9-4116-a575-667d31fa060d
    internal-label: APIs
subfeature_v2:
  - id: cf1396d8-ab85-4e93-b35d-d9b573024abf
    internal-label: REST APIs
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: d378ca77-2da1-4f39-ad92-1917fe974a38
    internal-label: Experienced
source-git-commit: 4768ecb20d4d9c70452ae084256928261f3a80eb
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 44%
---
# API ヘルプ - 変数にアクセストークンを設定する方法

Postman アプリケーションを設定し、変数を活用して、再利用目的でデータを変数に保存する方法について説明します。 また、最初のMarketo Engage REST API呼び出しを行ってアクセストークンを取得する方法についても説明します。

>[!PREREQUISITES]
>
>このビデオを開始する前に、AOI ロールを持つAPIのみのユーザー名を作成し、Launchpad サービスを作成します。 次の記事の手順に従います。
>
>* [API 専用ユーザーのロールの作成](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user-role){target="_blank"}
>
>* [API 専用ユーザーの作成](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/users-and-roles/create-an-api-only-user){target="_blank"}
>
>* [REST API で使用するカスタムサービスの作成](https://experienceleague.adobe.com/ja/docs/marketo/using/product-docs/administration/additional-integrations/create-a-custom-service-for-use-with-rest-api){target="_blank"}

**このビデオで使用されている参照：**

* Marketo認証エンドポイント：`{{{}base_url{}}}/identity/oauth/token?grant_type=client_credentials&client_id={{{}client_id{}}}&client_secret={{{}client_secret{}}}`

* 応答の本文からaccess_tokenを取得するJS スクリプト（「スクリプト：」タブの下に配置）:

```
var jsonData = pm.response.json();
pm.environment.set("access_token", jsonData.access_token);
```

* [Marketo Engage Developers ドキュメント](https://experienceleague.adobe.com/ja/docs/marketo-developer/marketo/rest/authentication){target="_blank"}

>[!VIDEO](https://video.tv.adobe.com/v/3429275/?learn=on)
