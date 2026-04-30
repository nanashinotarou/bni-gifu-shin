# Cursorタスク：wireframe_chirashi.html 追加セクション実装

作成日：2026-04-27  
対象ファイル：`wireframe_chirashi.html`（同フォルダ内）  
デザイナー向け複製（`デザイナー向け_チラシ制作/wireframe_chirashi.html`）も同様に更新すること。

---

## 背景

参考資料（プログレスチャプターPDF）と元サイト（innocent-web.com/gifu_shin/）を照合した結果、  
ワイヤーフレームに以下3セクションが抜けていることが判明。今回追加する。

---

## 現在の構成 → 更新後の構成

| 旧ブロック | 新ブロック | 変更 |
|---|---|---|
| [A] Header | [A] Header | 変更なし |
| | **[B] BNIとは** | **新規追加** |
| | **[C] 用語解説** | **新規追加** |
| [C] President | **[D] プレジデント** | **メッセージ本文を追記** |
| [B] Meeting info | [E] 例会情報 | 変更なし（ラベルのみ [B]→[E] に変更） |
| | **[F] 当日の流れ** | **新規追加** |
| [D] Contact | [G] Contact | 変更なし（ラベルのみ変更） |
| [E] Members | [H] Members | 変更なし（ラベルのみ変更） |
| [F] Footer | [I] Footer | 変更なし（ラベルのみ変更） |

---

## 追加・更新セクションの詳細

### [B] BNIとは（新規追加）

[A] Header ブロックの直後に挿入する。

```html
<!-- [B] BNIとはブロック -->
<section class="wf-block">
  <div class="wf-label">[B] What is BNI</div>
  <div class="wf-content" style="font-weight:bold; font-size:16px; color:#333; margin-bottom:10px;">BNIとは</div>
  <div class="wf-content">
    BNIは1985年にアイヴァン・マイズナー博士により創設された世界最大級のビジネス・リファーラル組織です。
    「ギバーズゲイン（Givers Gain®）」という理念に基づき、「与えるものは与えられる」という考え方で運営されています。
    経営者や事業オーナーが信頼関係を築き、相互にリファーラルを提供し合うことで、全メンバーが良い結果を得られる仕組みです。
  </div>
  <div class="wf-annotation">注釈：テキストは現行サイト（innocent-web.com/gifu_shin/）より転記。クライアント確認後に文言調整可。</div>
</section>
```

---

### [C] 用語解説（新規追加）

[B] BNIとはブロックの直後に挿入する。

```html
<!-- [C] 用語解説ブロック -->
<section class="wf-block">
  <div class="wf-label">[C] Glossary</div>
  <div class="wf-content" style="font-weight:bold; font-size:16px; color:#333; margin-bottom:10px;">よく使う用語の解説</div>
  <table class="glossary-table">
    <tr>
      <th>カテゴリー</th>
      <td>専門分野（職種）のこと。BNIでは各分野から1名のみチャプターへの加入が認められています。</td>
    </tr>
    <tr>
      <th>チャプター</th>
      <td>世界中に11,000を超えるBNIのビジネスチームのこと。このチャプターは「真チャプター」です。</td>
    </tr>
    <tr>
      <th>リファーラル</th>
      <td>メンバーが他のメンバーに対して、見込み客の紹介やビジネスの機会を提供すること。</td>
    </tr>
    <tr>
      <th>1to1</th>
      <td>メンバー同士がお互いのビジネスや人柄を理解し合う、1対1のビジネスミーティング。</td>
    </tr>
    <tr>
      <th>トレーニング</th>
      <td>BNIの活用方法やビジネススキルを学ぶための、メンバー限定のプログラム。</td>
    </tr>
  </table>
  <div class="wf-annotation">注釈：用語・解説文は現行サイトより転記。クライアント確認後に文言調整可。</div>
</section>
```

**スタイル追加（`<style>` 内に追記）：**

```css
.glossary-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 8px;
  font-size: 13px;
}
.glossary-table th {
  text-align: left;
  white-space: nowrap;
  padding: 8px 16px 8px 0;
  font-weight: bold;
  color: #333;
  vertical-align: top;
  width: 120px;
}
.glossary-table td {
  padding: 8px 0;
  color: #555;
  line-height: 1.6;
  border-bottom: 1px solid #eee;
}
```

---

### [D] プレジデントブロック（メッセージ本文追記）

既存の [C] プレジデントブロックを [D] にリラベルし、`ひとこと` の下にメッセージ本文を追加する。

追加する内容（`ひとこと` 行の直下）：

```html
<div style="margin-top:10px; font-size:13px; color:#555; line-height:1.7;">
  第5期のテーマは「覚醒」。真チャプター立ち上がり1年半が経ち、メンバーが初心に帰り真の文化を作ることで
  「本気でビジネスを応援する」姿勢を掲げています。
</div>
```

注釈にも「メッセージ本文は現行サイトより転記。写真は backup_images/itotomomi.jpg を使用予定。」を追記。

---

### [F] 当日の流れ（新規追加）

[E] 例会情報ブロックの直後に挿入する。  
⚠️ 時刻はすべて仮。プログレスチャプターの構成を8:30〜10:00に読み替えたもの。クライアント確認必須。

```html
<!-- [F] 当日の流れ -->
<section class="wf-block">
  <div class="wf-label">[F] Schedule</div>
  <div class="wf-content" style="font-weight:bold; font-size:16px; color:#333; margin-bottom:10px;">当日の流れ</div>
  <table class="schedule-table">
    <tr>
      <td class="time">8:20</td>
      <td>Zoomよりご入室いただき、「待機室」でお待ちください。</td>
    </tr>
    <tr>
      <td class="time">8:30</td>
      <td>【開始】招待者のほか、メンバー数人とお話しいただく時間を設けております。</td>
    </tr>
    <tr>
      <td class="time">8:35</td>
      <td>
        定例会本番スタート。簡単にご挨拶いただきます。<br>
        リーダーシップチーム紹介、BNIの目的と概要紹介、学習コーナー等に続き、<br>
        各メンバーのビジネスを全員が理解し営業できるよう、1人1分間プレゼンを行います。<br>
        <strong>ビジター様にも、ご自身のお仕事を1分間で紹介していただく時間を設けています。</strong>
      </td>
    </tr>
    <tr>
      <td class="time">9:10</td>
      <td>ブレイクアウトルームにて、新規顧客の紹介が生まれる様子をご覧ください。メインプレゼンテーション、メンバーへの推薦や承認などが行われます。</td>
    </tr>
    <tr>
      <td class="time">9:35</td>
      <td>各メンバーから全員へ、今週の貢献発表。</td>
    </tr>
    <tr>
      <td class="time">9:45</td>
      <td>本日ご参加いただいたご感想をお聞かせください。</td>
    </tr>
    <tr>
      <td class="time">9:50</td>
      <td>BNIへのご質問や、紹介してほしい方などをお伺いします。個別に話したいメンバーがいましたらお気軽にお知らせください。</td>
    </tr>
    <tr>
      <td class="time">10:00</td>
      <td>【終了】ご参加いただきありがとうございました。</td>
    </tr>
  </table>
  <div class="wf-annotation">
    注釈：時刻はすべて仮（プログレスチャプターPDF記載のスケジュールを8:30〜10:00に読み替えたもの）。<br>
    実際のタイムスケジュールはクライアント（真チャプター）に確認して差し替えること。
  </div>
</section>
```

**スタイル追加（`<style>` 内に追記）：**

```css
.schedule-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 8px;
  font-size: 13px;
}
.schedule-table tr {
  border-bottom: 1px solid #eee;
}
.schedule-table td {
  padding: 10px 8px;
  color: #555;
  line-height: 1.6;
  vertical-align: top;
}
.schedule-table td.time {
  font-weight: bold;
  color: #333;
  white-space: nowrap;
  padding-right: 20px;
  width: 50px;
}
```

---

## 更新後の注意事項

- 既存ブロックのラベル（`[B]〜[F]`）は `[E]〜[I]` に振り直すこと（HTML内のコメントと `wf-label` テキスト両方）
- `デザイナー向け_チラシ制作/wireframe_chirashi.html` にも同じ変更を適用すること
- 全体的なスタイル（`.wf-block`, `.wf-annotation` など）は既存定義を踏襲し、追加スタイルのみ足すこと

---

## 変更しないもの

- CTA（「ご興味のある方はお気軽に」）の文言・配置
- メンバーグリッド（15名）
- フッター
- ヘッダー
