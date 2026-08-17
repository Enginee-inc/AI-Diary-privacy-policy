# プライバシーポリシー（AI Diary）

最終更新日：2026年7月29日

株式会社Enginee（以下「当社」）は、当社が提供するアプリケーション「AI Diary」（以下「本サービス」）における個人情報の取り扱いについて、本プライバシーポリシー（以下「本ポリシー」）のとおり定めます。

本サービスは、AIキャラクターとの音声会話を通じて日記を作成・保存するアプリです。その性質上、**お客様の発話内容を外部のAIサービスへ送信して処理し、会話から得られたお客様に関する情報を保存して次回以降の会話に利用します**。本ポリシーでは、その内容をできる限り具体的に説明します。

当社全体の個人情報保護方針、保有個人データの開示・訂正・利用停止等のご請求手続き、および組織としての安全管理措置については、[株式会社Enginee プライバシーポリシー／個人情報の取り扱いについて](https://orchid-spring-653.notion.site/189b380b38834593bf9eed20a484d50a)（以下「全社ポリシー」）に定めるところによります。本ポリシーは全社ポリシーを本サービスに即して具体化したものであり、本サービスに関して両者の内容が異なる場合は本ポリシーが優先します。

---

## 1. 事業者情報・お問い合わせ窓口

| 項目 | 内容 |
|---|---|
| 事業者名 | 株式会社Enginee |
| 住所 | 〒112-0004　東京都文京区後楽2丁目3番11号　FLAT21 101号室 |
| 代表者 | 代表取締役　小山 賞馨 |
| 個人情報保護管理者 | コーポレート統括本部　情報セキュリティ担当 |

**個人情報お問い合わせ窓口**

- お問い合わせフォーム：https://www.enginee.co.jp/form （お問い合わせ種別「プライバシーポリシー・個人情報取扱いについて」を選択してください）
- メール：legal@enginee.co.jp
- 受付時間：10:00〜16:00（土・日・祝日・年末年始を除く）

※お客様との通話は、内容確認の目的で録音させていただく場合がございます。

---

## 2. 取得する情報

本サービスは、機能の提供のために以下の情報を取得・保存します。

### アカウント情報

- メールアドレス、表示名（Apple または Google でサインインしたときに取得します）
- 認証識別子（Firebase のユーザーID、および Apple / Google のユーザーID）

Apple の「メールアドレスを隠す」を選択した場合、当社が取得するのは Apple が発行する転送用アドレスのみで、お客様の実際のメールアドレスは取得しません。

### 一時的な匿名アカウント

サインインが完了する前の段階では、動作のために匿名アカウントを一時的に作成します。サインインされないまま24時間が経過した匿名アカウントは、サーバー側で自動的に削除されます。

### 会話・日記データ

- 音声認識によって文字起こしされた会話テキスト
- AI が生成した日記の要約、気分（mood）の分類、話題（topics）、天気カテゴリ
- 選択したキャラクター（ペルソナ）、通話の開始日時・所要時間

### 記憶プロフィール・ベクトル記憶

会話から生成される、お客様に関する要約情報と、日記を検索するための数値ベクトルです。詳しくは第4条をご覧ください。

### ニックネーム・自己紹介

- **ニックネーム**は端末の安全な保管領域（iOS の Keychain / Android の Keystore）に保存されます。キャラクターがお客様を名前で呼べるようにするため、会話の応答を生成する都度サーバーへ送信されますが、送信された値をサーバーに保存することはありません。
- **初回設定時にご入力いただく自己紹介**（お客様自身のこと・お仕事や学業・いま取り組んでいること）は、キャラクターが最初からお客様を知っている状態で会話を始められるようにするため、**当社サーバー上の記憶プロフィール（第4条）へ保存されます**。保存後、端末側の控えは削除されます。保存された内容は、アプリの「{キャラクター名}がおぼえていること」画面からいつでも確認・編集・削除できます。

### 端末内にのみ保存される情報

- 「帰宅したら電話」機能で登録した自宅の座標（第5条）

この情報は端末の安全な保管領域（iOS の Keychain）にのみ保存され、当社サーバーには送信も保存もしません。

### 端末の機能を通じて取得する情報

- マイクからの音声（音声認識のためにのみ使用し、当社サーバーには録音・保存しません。第3条）
- 位置情報（「帰宅したら電話」機能を有効にした場合のみ。第5条）
- プッシュ通知トークン（「着信でおしゃべり」機能を有効にした場合のみ。iOS では VoIP通知トークン、Android では FCM 登録トークン。第7条）

### 通信時に自動的に送信される情報

- IPアドレス（日記に天気を記録するための地域推定に使用します。第6条）

### 利用状況データ

- 通話の開始日時・最終利用日時（1日1回の利用回数制限などの管理のため）
- アプリ内の主要な操作イベント（第8条）

**本サービスは、広告・行動トラッキングを目的とした解析を行わず、サードパーティの解析SDK・広告SDKを一切搭載していません。**

---

## 3. 音声・会話データの取り扱い（重要）

本サービスは音声会話を実現するために、以下の処理を行います。お客様の発話内容は、これらの処理のために外部サービスへ送信されます。

1. **音声認識（文字起こし）**：マイク音声は、iOS では Apple、Android では Google が提供する端末の音声認識機能で文字に変換されます。認識精度の都合上、音声データが各OS提供事業者のサーバーへ送信される場合があります。当社は音声そのものを取得・保存しません。
2. **AI応答の生成**：文字起こししたテキストと会話履歴は、AI の応答を生成するためにクラウドの大規模言語モデル（LLM）へ送信されます。このとき、第4条の記憶プロフィールと関連する過去の日記も併せて送信されます。
3. **音声合成（読み上げ）**：AI の応答テキストは、音声に変換するため音声合成サービスへ送信されます。
4. **日記の要約**：通話終了時に、会話内容を要約して日記を作成するため、会話テキストが LLM へ送信されます。
5. **記憶の索引付け**：作成された日記は、あとから関連する記憶を探し出せるようにするため、数値ベクトル（埋め込み）へ変換されます。この処理にも日記テキストが外部サービスへ送信されます。
6. **日記を用いた分析機能**：「ぶんせき」画面のふりかえり・話題の発見・月次ダイジェスト、および「日記への質問」機能では、対象期間の日記の要約や本文が LLM へ送信されます。日記の意味検索・「似ている日」の表示でも、検索文や日記の要約が埋め込みへ変換されます。**これらはお客様が当該画面を開いた、または操作したときにのみ実行されます。**

これらの外部サービスの一部は日本国外に所在します（第11条を参照）。各サービスへ送信されたデータは、各社の利用規約に基づき本サービスへの応答生成のためにのみ処理され、当社の確認する限り、各社の生成AIモデルの学習には利用されません。

---

## 4. AIによるパーソナライズと「記憶」（重要）

本サービスは、会話を重ねるほどお客様のことを理解したキャラクターになることを目的としています。そのために、以下の2種類の「記憶」を当社サーバー（お客様ご本人のアカウント配下）に保存します。

### (1) 記憶プロフィール

通話が終わるたびに、その日の会話から**お客様がどのような方かという要約**を AI が生成し、次の6つのカテゴリに整理して蓄積・更新します。

- 本人のこと／人間関係／仕事・学業／進行中のこと／好み／よく話す話題

これに加えて、「いまのお客様」を1〜2文で表したリード文と、直近の出来事の記録（最大8件）を保持します。これらは次回以降の会話の冒頭でキャラクターに渡され、「知っている前提」で話せるようにするために使われます。

### (2) ベクトル記憶

作成された日記は、意味の近さで検索できるよう数値ベクトルへ変換して保存されます。会話中のお客様の発話に関連する過去の日記や、「先週なに話したっけ」といった日付の指定があったときに、該当する日記を探し出してキャラクターに渡すために使われます。

### お客様による確認・訂正・削除

- **閲覧・編集**：アプリの「{キャラクター名}がおぼえていること」画面で、記憶プロフィールの全文をいつでも確認でき、ご自身で書き換え・削除ができます。
- **一括削除**：マイページの「ぜんぶ忘れてもらう」から、ベクトル記憶と記憶プロフィールをまとめて削除できます（日記そのものは残ります）。
- これらの記憶はお客様ご本人のアカウント配下にのみ保存され、他のお客様の会話に利用されることはありません。また、AIモデルの学習にも利用されません。

---

## 5. 位置情報の取り扱い（重要）

位置情報を利用するのは、**「帰宅したら電話」機能（任意・初期設定はオフ）を有効にした場合のみ**です。

- **自宅の座標は端末の外に出ません。** 登録された自宅の座標は端末の安全な保管領域（iOS の Keychain）にのみ保存され、当社サーバーへ送信することも、保存することもありません。地図や座標をアプリ画面に表示することもありません。
- **出入りの判定は端末のOSが行います。** 自宅の周辺に設定した円への出入りは、端末のOS（ジオフェンス機能）が判定します。当社サーバーが受け取るのは「入った／出た」という事実と、その発生時刻だけです。**緯度経度を受け取る項目は、サーバーの受信仕様そのものに存在しません。**
- **移動履歴は保持しません。** 帰宅の検知によって作成された着信の予約は、着信後に削除され、帰宅時刻の履歴として蓄積されることはありません。
- **オフにすると削除されます。** 機能をオフにすると、OSへのジオフェンス登録を解除し、端末に保存された自宅の座標も削除します。
- OSの位置情報の許可は、いつでも端末の「設定」アプリから取り消すことができます。

---

## 6. 天気情報の取得とIPアドレス

日記に「その日の天気」を残すため、日記の作成時に、通信元のIPアドレスからおおまかな地域を推定し、その地域の気象情報を取得します。

- IPアドレス、および推定された緯度経度は、**当社のデータベースにもアプリへの応答にも保存・返却しません**。日記に残るのは「晴れ」などの天気カテゴリの文字列だけです。
- 委託先は、IPアドレスから地域を推定する ipwho.is と、気象情報を提供する Open-Meteo です（第10条）。
- この機能は、サーバー側の設定によって停止することがあります。停止時は日記に天気が付かないだけで、他の機能に影響はありません。

---

## 7. 通知・着信

- **毎日のリマインダー通知**は、端末内でスケジュールされるローカル通知です。当社サーバーは関与せず、通知の内容が外部へ送信されることもありません。
- **「着信でおしゃべり」（着信画面での通話）**を有効にした場合、当社サーバーからプッシュ通知を経由して着信を配信するため、端末のプッシュ通知トークンをお客様のアカウント配下に保存します（iOS は Apple のプッシュ通知サービス（APNs）、Android は Firebase Cloud Messaging（FCM）を利用します）。併せて、着信を鳴らす時刻（HH:MM）と、発信者として表示するキャラクター名を保存します。これらのトークンは、アプリから読み取れない領域に保存します。
- **「帰宅したら電話」**を有効にした場合も、同じ仕組みで着信を配信します（第5条）。
- 着信は、深夜などにお客様の意図せず鳴ることを防ぐため、サーバー側で許可された時間帯（既定 7:00〜23:30 日本時間）と1日あたりの回数に制限を設けています。
- 通知・着信はいつでもマイページからオフにできます。オフにすると、上記の予約と設定は削除されます。

---

## 8. 利用状況の計測（アナリティクス）

サービスの継続的な改善のため、アプリ内での主要な操作を、**当社が運用するサーバー（Firebase Functions / Firestore）へ**記録します。第三者の解析サービスや広告ネットワークは一切利用していません。

- **記録する内容**：イベント名（アプリ起動、通話開始、通話完了、日記保存、通知許可の可否など）、発生時刻、選択したキャラクター、通話の所要時間、通話セッションの識別子、処理が成功したかどうか、といった項目です。
- **記録しない内容**：会話の内容、日記の本文、ニックネーム、自己紹介など、お客様個人を特定しうる情報はイベントに含めません。
- イベントはお客様ご本人のアカウント配下に保存され、アカウントを削除すると一緒に削除されます。
- 当社の管理用ダッシュボードに表示されるのは集計された数値のみで、個々のユーザーIDや会話内容が表示されることはありません。

---

## 9. 利用目的

当社は、取得した情報を以下の目的で利用します。

1. お客様の認証およびアカウント管理
2. 音声会話、日記の作成・保存・閲覧といった本サービスの機能の提供
3. 日記をもとにしたふりかえり・分析・検索機能の提供（第3条6項）
4. 会話のパーソナライズ（記憶プロフィールおよび過去の日記の参照。第4条）
5. お客様が有効にした場合の、通知および着信の配信（第5条・第7条）
6. 利用回数制限の管理をはじめとする、不正利用・濫用の防止
7. 障害対応、およびサービスの維持・改善（第8条）
8. お客様からのお問い合わせへの対応
9. 法令に基づく対応

これらの範囲を超えて個人情報を利用する場合は、改めて利用目的をお知らせし、ご同意をいただきます。

---

## 10. 第三者サービス（委託先）

本サービスは、機能の提供のために以下の事業者へ情報の処理を委託しています。当社は、法令に基づく場合を除き、お客様の個人情報を第9条の利用目的の範囲を超えて第三者へ提供せず、また販売もしません。

| サービス | 提供者 | 用途 | 送信される主な情報 |
|---|---|---|---|
| Firebase（Authentication / Firestore / Cloud Functions） | Google LLC（米国） | 認証、データ保存、サーバー処理 | アカウント情報、会話・日記テキスト、記憶プロフィール、利用状況イベント |
| Gemini API（LLM・音声合成・埋め込み） | Google LLC（米国） | 会話応答の生成、日記の要約、読み上げ音声の合成、記憶の索引付けと検索 | 会話テキスト、日記テキスト、記憶プロフィール、応答テキスト |
| 端末の音声認識 | Apple Inc.（米国）／Google LLC（米国） | 音声の文字起こし | マイク音声 |
| Apple Push Notification service（APNs）※iOS | Apple Inc.（米国） | 着信の配信 | VoIP通知トークン、着信に表示するキャラクター名 |
| Firebase Cloud Messaging（FCM）※Android | Google LLC（米国） | 着信の配信 | FCM 登録トークン、着信に表示するキャラクター名 |
| ipwho.is | ipwhois.io | IPアドレスからのおおまかな地域の推定 | IPアドレス |
| Open-Meteo | OpenMeteo GmbH（スイス） | 気象情報の取得 | 推定されたおおまかな緯度経度（個人を特定する情報は含みません） |

各社における個人情報の取り扱いについては、各社のプライバシーポリシーをご確認ください。

- Google：https://policies.google.com/privacy
- Apple：https://www.apple.com/legal/privacy/
- ipwho.is（ipwhois.io）：https://ipwhois.io/privacy
- Open-Meteo：https://open-meteo.com/en/terms

---

## 11. 個人データの外国にある第三者への提供

第10条のとおり、本サービスはお客様の情報を日本国外に所在する事業者へ送信します。これは本サービスの音声会話、データ保存、および付随機能の提供に必要なものです。

- **アメリカ合衆国**：Google LLC、Apple Inc.
- **スイス連邦**：OpenMeteo GmbH

なお、ipwho.is（ipwhois.io）については、提供者の所在国が公表されていないため、当社は所在国を特定できておりません。同社へ送信されるのは通信元のIPアドレスのみで、氏名・メールアドレス・会話内容などは一切送信されません。当社は、同社が公表するプライバシーポリシーを確認したうえで委託しています。

各国における個人情報の保護に関する制度、および移転先が講じる保護措置に関する情報のご請求は、第1条の窓口で承ります。

---

## 12. データの保存期間と削除

- 会話記録、日記、記憶プロフィール、ベクトル記憶は、お客様が削除するまで保存されます。
- **記憶のみの削除**：マイページの「ぜんぶ忘れてもらう」から、記憶プロフィールとベクトル記憶をまとめて削除できます（日記は残ります）。
- **日記の削除**：日記は1件ずつ削除できます。
- **アカウントの削除**：マイページの「アカウント削除」から、アカウントと、その配下のすべてのデータ（日記、会話記録、記憶、利用状況イベント、通知の設定と予約）を削除できます。**この操作は取り消せません。** Apple でサインインされている場合は、併せて Apple 側との連携も失効させます。
- **削除後に残る記録**：アカウントの削除と再作成による利用回数制限の回避を防ぐため、認証プロバイダのユーザーIDをソルト付きハッシュ化した識別子（元のIDを復元できません）と、最後に通話した日（日付の粒度のみで、時刻は含みません）を保持することがあります。**この記録は削除から90日で自動的に失効します。**
- **匿名アカウント**：サインインされないまま24時間が経過した一時的な匿名アカウントは、自動的に削除されます。

---

## 13. 安全管理措置

本サービスにおいて、当社は以下の措置を講じています。

- 端末とサーバーの間の通信はすべて TLS（HTTPS）により暗号化しています。
- 外部サービスのAPIキーはすべてサーバー側で管理し、アプリ（クライアント）には保持しません。
- データベースはアクセス制御により、原則としてお客様ご本人だけが自身のデータを読み取れるよう構成しています。書き込みはすべてサーバーを経由し、アプリからの直接の書き込みを禁止しています。
- 端末内では、ニックネームおよび自宅の座標をOSの安全な保管領域（iOS の Keychain / Android の Keystore）に保存し、会話ログと認証情報はその領域に保管した鍵で暗号化したうえで保存しています。
- 不正利用・濫用およびコストの異常な増大を防ぐため、サーバー側にレート制限を設けています。

当社の組織的・人的・物理的安全管理措置、および外的環境の把握については、全社ポリシー「4. 安全管理措置」に定めるところによります。

---

## 14. お客様の権利とご請求の手続き

お客様は、ご自身の個人情報について、利用目的の通知、開示、内容の訂正・追加・削除、利用の停止・消去、第三者への提供の停止、および第三者提供記録の開示を請求する権利を有します。

**アプリ内で直接行えること**

- 記憶プロフィールの確認・編集・削除（「{キャラクター名}がおぼえていること」画面）
- 記憶の一括削除（マイページ「ぜんぶ忘れてもらう」）
- 日記の編集・削除
- アカウントとすべてのデータの削除（マイページ「アカウント削除」）
- 通知・着信・位置情報を用いた機能のオン／オフ

**それ以外のご請求**

上記以外のご請求については、全社ポリシー「2.」に定める手続きに従い、第1条の窓口までご連絡ください。ご請求内容の確認後、当社所定の請求様式をお送りします。ご本人および代理人であることの確認をさせていただきます。当社所定の手数料（500円）および請求にかかる郵送費等はご請求者様のご負担となります。

なお、保有個人データの削除・利用停止等をお求めの場合、本サービスの提供ができなくなることをご了承ください。

---

## 15. 欧州経済領域（EEA）・英国のお客様へ（GDPR）

GDPR が適用されるお客様について、当社は個人データの管理者です。処理の法的根拠は、サービス提供のための契約の履行、お客様の同意（位置情報・通知・着信など、お客様が任意で有効にする機能）、および不正防止に関する当社の正当な利益です。

お客様は、アクセス・訂正・消去・処理の制限・データポータビリティ・異議申立ての権利、および監督機関へ苦情を申し立てる権利を有します。日本国外への移転は、サービス提供に必要な範囲で、適切な保護措置のもとに行われます。

---

## 16. カリフォルニア州のお客様へ（CCPA／CPRA）

当社はお客様の個人情報を販売・共有しません。カリフォルニア州のお客様は、収集した個人情報の開示および削除を請求する権利、ならびに権利行使を理由に差別されない権利を有します。ご請求は第1条の窓口で承ります。

---

## 17. 子どもの個人情報

本サービスは13歳未満（EEA等、適用法域によっては16歳未満）の子どもを対象としていません。対象年齢未満の方は本サービスを利用しないでください。対象年齢未満の方の個人情報を取得したことが判明した場合、当社は速やかに当該情報を削除します。

---

## 18. 本ポリシーの変更

当社は、法令の変更やサービス内容の変更に応じて本ポリシーを改定することがあります。重要な変更を行う場合は、アプリ内またはその他の適切な方法で告知します。

---

## 19. お問い合わせ

本ポリシーに関するお問い合わせは、第1条に記載の窓口までご連絡ください。

---
---

# Privacy Policy (AI Diary)

Last updated: July 29, 2026

Enginee Inc. (the "Company," "we," or "us") sets out in this Privacy Policy (the "Policy") how we handle personal information of users ("you") of our application "AI Diary" (the "Service").

The Service is an application for creating and saving diary entries through voice conversations with AI characters. Given the nature of the Service, **we transmit what you say to external AI services for processing, and we store information about you derived from those conversations and use it in subsequent conversations.** This Policy explains that processing as concretely as we can.

Our company-wide personal information protection policy, the procedures for requesting disclosure, correction, or suspension of use of retained personal data, and our organizational security measures are set out in the [Enginee Inc. Privacy Policy / Handling of Personal Information](https://orchid-spring-653.notion.site/189b380b38834593bf9eed20a484d50a) (the "Corporate Policy"). This Policy makes the Corporate Policy concrete for the Service; where the two differ with respect to the Service, this Policy prevails.

---

## 1. Business Information and Contact

| Item | Details |
|---|---|
| Company name | Enginee Inc. (株式会社Enginee) |
| Address | FLAT21 Room 101, 2-3-11 Koraku, Bunkyo-ku, Tokyo 112-0004, Japan |
| Representative | Shokei Koyama, Representative Director |
| Personal information protection manager | Information Security, Corporate Division |

**Personal Information Inquiry Desk**

- Inquiry form: https://www.enginee.co.jp/form (please select the category "Privacy Policy / Handling of Personal Information")
- Email: legal@enginee.co.jp
- Hours: 10:00–16:00 JST (excluding weekends, public holidays, and the year-end/New Year period)

Please note that calls with customers may be recorded for the purpose of verifying their content.

---

## 2. Information We Collect

The Service collects and stores the following information in order to provide its functionality.

### Account information

- Email address and display name (obtained when you sign in with Apple or Google)
- Authentication identifiers (your Firebase user ID and your Apple / Google user ID)

If you use Apple's "Hide My Email," we receive only the relay address issued by Apple, not your actual email address.

### Temporary anonymous accounts

Before sign-in completes, a temporary anonymous account is created so the app can function. Anonymous accounts that remain unsigned-in for 24 hours are automatically deleted server-side.

### Conversation and diary data

- Transcribed text from your voice conversations
- AI-generated diary summaries, mood classifications, topics, and weather category
- The character (persona) you selected, and the start time and duration of each call

### Memory profile and vector memories

Summarized information about you generated from your conversations, and numerical vectors used to search your diary entries. See Section 4.

### Nickname and self-introduction

- **Your nickname** is stored in your device's secure storage (iOS Keychain / Android Keystore). It is transmitted to the server each time a response is generated, so that the character can address you by name, but the transmitted value is not stored on the server.
- **The self-introduction you provide during initial setup** (about yourself, your work or studies, and what you are currently working on) **is stored in your memory profile on our servers** (Section 4), so that the character can begin conversations already knowing something about you. Once stored, the local copy on your device is deleted. You can review, edit, or delete the stored content at any time on the "What {character} remembers" screen.

### Information stored only on your device

- The home coordinates registered for the "Call me when I get home" feature (Section 5)

This information is stored only in your device's secure storage (iOS Keychain) and is never transmitted to, or stored on, our servers.

### Information obtained via device features

- Audio from your microphone (used solely for speech recognition; we do not record or store the audio on our servers — Section 3)
- Location information (only if you enable "Call me when I get home" — Section 5)
- Push notification token (only if you enable incoming calls; a VoIP push token on iOS, an FCM registration token on Android — Section 7)

### Information transmitted automatically when you communicate with us

- IP address (used to estimate an approximate region so that weather can be recorded in your diary — Section 6)

### Usage data

- Call start timestamps and last-used date (used to manage the once-per-day usage limit and similar controls)
- Key in-app events (Section 8)

**The Service does not perform analytics for advertising or behavioral tracking, and does not incorporate any third-party analytics or advertising SDKs.**

---

## 3. How We Handle Voice and Conversation Data (Important)

To enable voice conversations, the Service performs the following processing. Your spoken content is transmitted to external services for each of these purposes.

1. **Speech recognition (transcription):** Microphone audio is converted to text using the on-device speech recognition functionality provided by Apple on iOS and Google on Android. For accuracy reasons, audio data may be transmitted to the servers of these OS providers. We do not obtain or store the audio itself.
2. **AI response generation:** Transcribed text and conversation history are sent to cloud-based large language models (LLMs) to generate AI responses. Your memory profile (Section 4) and relevant past diary entries are sent along with them.
3. **Speech synthesis (text-to-speech):** AI response text is sent to a speech synthesis service to convert it into audio.
4. **Diary summarization:** At the end of a call, conversation text is sent to an LLM to create a diary summary.
5. **Memory indexing:** Diary entries are converted into numerical vectors (embeddings) so that relevant memories can be retrieved later. This also involves sending diary text to an external service.
6. **Diary-based analysis features:** The review, topic-discovery, and monthly digest features on the "Analysis" screen, as well as the "Ask your diary" feature, send summaries or full text of diary entries from the relevant period to an LLM. Semantic diary search and the "similar days" feature also convert your query and diary summaries into embeddings. **These run only when you open or interact with the relevant screen.**

Some of these external services are located outside Japan (see Section 11). Data sent to each service is processed solely for the purpose of generating responses to the Service, in accordance with each provider's terms of use, and to the best of our knowledge is not used to train those providers' generative AI models.

---

## 4. AI Personalization and "Memory" (Important)

The Service is designed so that the character understands you better the more you talk. To achieve this, we store two kinds of "memory" on our servers, under your own account.

### (1) Memory profile

At the end of each call, an AI generates **a summary of who you are** from that day's conversation and accumulates it under six categories:

- About you / Relationships / Work and study / Things in progress / Preferences / Recurring topics

In addition, we retain a one- or two-sentence lead describing "who you are right now" and a record of recent events (up to eight entries). These are provided to the character at the start of subsequent conversations so that it can speak with knowledge of you.

### (2) Vector memories

Diary entries are converted into numerical vectors and stored so they can be searched by semantic similarity. They are used to find past entries relevant to what you are saying, or to answer date-based questions such as "what did we talk about last week?"

### Your ability to review, correct, and delete

- **Review and edit:** You can view the full text of your memory profile at any time on the "What {character} remembers" screen and edit or delete it yourself.
- **Bulk deletion:** You can delete your vector memories and memory profile together from "Forget everything" in Settings (your diary entries remain).
- These memories are stored only under your own account and are never used in other users' conversations. They are also not used to train AI models.

---

## 5. Location Information (Important)

We use location information **only if you enable the "Call me when I get home" feature (optional; off by default).**

- **Your home coordinates never leave your device.** The registered coordinates are stored only in your device's secure storage (iOS Keychain) and are never transmitted to, or stored on, our servers. We also never display a map or coordinates in the app.
- **Entry and exit are determined by your device's OS.** Crossing the boundary of the circle set around your home is detected by the device's OS (geofencing). All our server receives is the fact that you entered or exited, and the time it occurred. **There is no field in our server's request specification that accepts latitude or longitude.**
- **We do not retain a movement history.** The scheduled call created by a home-arrival detection is deleted once the call is placed, and is not accumulated as a history of arrival times.
- **Turning the feature off deletes the data.** Disabling the feature removes the geofence registration from the OS and deletes the home coordinates stored on your device.
- You can revoke the OS location permission at any time from your device's Settings app.

---

## 6. Weather Information and IP Addresses

To record "the weather that day" in your diary, we estimate an approximate region from the IP address of your connection when a diary entry is created, and retrieve weather information for that region.

- The IP address and the estimated latitude/longitude are **neither stored in our database nor returned to the app.** All that remains in your diary is a weather category string such as "sunny."
- Our processors are ipwho.is (IP-to-region estimation) and Open-Meteo (weather data) — see Section 10.
- This feature may be disabled by server-side configuration. When disabled, diary entries simply have no weather attached; no other functionality is affected.

---

## 7. Notifications and Incoming Calls

- **Daily reminder notifications** are local notifications scheduled on your device. Our servers are not involved, and the content of these notifications is not transmitted externally.
- If you enable **incoming calls**, we store your device's push notification token under your account so that our server can deliver calls (via Apple Push Notification service (APNs) on iOS, and Firebase Cloud Messaging (FCM) on Android). We also store the time of day at which to ring (HH:MM) and the character name to display as the caller. These tokens are stored in an area that the app cannot read.
- If you enable **"Call me when I get home,"** calls are delivered through the same mechanism (Section 5).
- To prevent calls from ringing unintentionally — for example late at night — the server enforces a permitted time window (7:00–23:30 JST by default) and a limit on the number of calls per day.
- You can turn notifications and incoming calls off at any time in Settings. Doing so deletes the associated schedules and settings.

---

## 8. Usage Analytics

To continuously improve the Service, we record key in-app actions **on servers we operate ourselves** (Firebase Functions / Firestore). We do not use any third-party analytics service or advertising network.

- **What we record:** event names (app launch, call started, call completed, diary saved, notification permission granted or denied, and similar), timestamps, the character you selected, call duration, a call session identifier, and whether processing succeeded.
- **What we do not record:** conversation content, diary text, nicknames, self-introductions, or any other information that could identify you personally is never included in these events.
- Events are stored under your own account and are deleted together with your account.
- Our internal dashboard displays only aggregate figures; it never displays individual user IDs or conversation content.

---

## 9. Purposes of Use

We use the information we collect for the following purposes:

1. Authenticating you and managing your account
2. Providing the Service's core features: voice conversations, and the creation, storage, and viewing of diary entries
3. Providing diary-based review, analysis, and search features (Section 3, item 6)
4. Personalizing conversations (memory profile and references to past diary entries — Section 4)
5. Delivering notifications and incoming calls, where you have enabled them (Sections 5 and 7)
6. Preventing fraud and abuse, including enforcement of usage limits
7. Responding to incidents and maintaining and improving the Service (Section 8)
8. Responding to your inquiries
9. Complying with applicable laws and regulations

If we wish to use personal information beyond these purposes, we will notify you of the new purpose and obtain your consent.

---

## 10. Third-Party Services (Processors)

The Service entrusts the processing of information to the following companies in order to provide its functionality. Except as required by law, we do not provide your personal information to third parties beyond the purposes described in Section 9, and we do not sell it.

| Service | Provider | Purpose | Primary data transmitted |
|---|---|---|---|
| Firebase (Authentication / Firestore / Cloud Functions) | Google LLC (USA) | Authentication, data storage, server processing | Account information, diary and conversation text, memory profile, usage events |
| Gemini API (LLM, speech synthesis, embeddings) | Google LLC (USA) | Conversation responses, diary summarization, speech synthesis, memory indexing and retrieval | Conversation text, diary text, memory profile, response text |
| On-device speech recognition | Apple Inc. (USA) / Google LLC (USA) | Voice transcription | Microphone audio |
| Apple Push Notification service (APNs) — iOS | Apple Inc. (USA) | Delivery of incoming calls | VoIP push token, character name shown for the call |
| Firebase Cloud Messaging (FCM) — Android | Google LLC (USA) | Delivery of incoming calls | FCM registration token, character name shown for the call |
| ipwho.is | ipwhois.io | Estimating an approximate region from an IP address | IP address |
| Open-Meteo | OpenMeteo GmbH (Switzerland) | Weather data | Estimated approximate coordinates (contains no personally identifying information) |

Please review each provider's privacy policy for details on how they handle personal information:

- Google: https://policies.google.com/privacy
- Apple: https://www.apple.com/legal/privacy/
- ipwho.is (ipwhois.io): https://ipwhois.io/privacy
- Open-Meteo: https://open-meteo.com/en/terms

---

## 11. Transfer of Personal Data to Third Parties in Foreign Countries

As described in Section 10, the Service transmits your information to companies located outside Japan. This is necessary to provide the Service's voice conversation, data storage, and related features.

- **United States:** Google LLC, Apple Inc.
- **Switzerland:** OpenMeteo GmbH

With respect to ipwho.is (ipwhois.io), the provider's country of operation is not publicly disclosed and we have therefore been unable to identify it. The only data transmitted to that provider is the IP address of your connection; no name, email address, or conversation content is transmitted. We reviewed the provider's published privacy policy before entrusting this processing to it.

For information about personal data protection regimes in the relevant countries and the safeguards applied by recipients, please contact us at the address in Section 1.

---

## 12. Retention Period and Deletion

- Conversation records, diary entries, memory profiles, and vector memories are retained until you delete them.
- **Deleting memories only:** "Forget everything" in Settings deletes your memory profile and vector memories together (diary entries remain).
- **Deleting diary entries:** Diary entries can be deleted individually.
- **Deleting your account:** "Delete Account" in Settings deletes your account and all data beneath it — diary entries, conversation records, memories, usage events, and notification settings and schedules. **This action cannot be undone.** If you signed in with Apple, we also revoke the linkage on Apple's side.
- **What remains after deletion:** To prevent circumvention of usage limits by deleting and re-creating an account, we may retain a salted SHA-256 hash of your authentication provider's user ID (from which the original ID cannot be recovered) together with the date of your last call (date granularity only; no time of day). **This record expires automatically 90 days after deletion.**
- **Anonymous accounts:** Temporary anonymous accounts that remain unsigned-in for 24 hours are deleted automatically.

---

## 13. Security Measures

For the Service, we have implemented the following measures.

- All communication between your device and our servers is encrypted using TLS (HTTPS).
- API keys for external services are managed exclusively on the server side and are never stored in the app (client).
- The database is configured with access controls so that, as a rule, only you can read your own data. All writes go through our servers; direct writes from the app are prohibited.
- On your device, your nickname and home coordinates are stored in the OS's secure storage (iOS Keychain / Android Keystore), and your conversation logs and authentication credentials are encrypted with a key held in that secure storage before being saved.
- Rate limits are enforced server-side to prevent abuse and runaway costs.

Our organizational, personnel, and physical security measures, and our assessment of the external environment, are set out in Section 4 of the Corporate Policy.

---

## 14. Your Rights and How to Exercise Them

You have the right to request notification of the purposes of use, disclosure, correction, addition, or deletion of content, suspension of use or erasure, suspension of provision to third parties, and disclosure of third-party provision records, with respect to your personal information.

**What you can do directly in the app**

- Review, edit, and delete your memory profile ("What {character} remembers" screen)
- Delete all memories at once ("Forget everything" in Settings)
- Edit and delete diary entries
- Delete your account and all associated data ("Delete Account" in Settings)
- Turn notifications, incoming calls, and location-based features on or off

**Other requests**

For requests other than the above, please contact the desk in Section 1, following the procedure set out in Section 2 of the Corporate Policy. After confirming the content of your request, we will send you our prescribed request form. We will verify that you are the individual concerned, or an authorized representative. Our prescribed fee (JPY 500) and any postage or similar costs associated with the request are borne by the requester.

Please note that if you request deletion or suspension of use of retained personal data, we may no longer be able to provide the Service to you.

---

## 15. For Users in the European Economic Area (EEA) and UK (GDPR)

For users to whom the GDPR applies, the Company is the data controller. The legal bases for processing are: performance of the contract to provide the Service; your consent (for optional features you enable, such as location, notifications, and incoming calls); and our legitimate interests in preventing fraud.

You have the rights of access, rectification, erasure, restriction of processing, data portability, and objection, as well as the right to lodge a complaint with a supervisory authority. Transfers outside Japan are made to the extent necessary to provide the Service and with appropriate safeguards in place.

---

## 16. For California Users (CCPA / CPRA)

We do not sell or share your personal information. California users have the right to request disclosure and deletion of the personal information we have collected about them, and the right not to be discriminated against for exercising these rights. Requests may be submitted at the contact address in Section 1.

---

## 17. Children's Personal Information

The Service is not intended for children under 13 years of age (or under 16 years of age in the EEA and other applicable jurisdictions). If you are below the applicable age, please do not use the Service. If we learn that we have obtained personal information from a person below the applicable age, we will delete it promptly.

---

## 18. Changes to This Policy

We may revise this Policy in response to changes in laws or in the content of the Service. If we make material changes, we will notify you within the app or by other appropriate means.

---

## 19. Contact

For inquiries regarding this Policy, please contact the desk listed in Section 1.
