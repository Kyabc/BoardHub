# 🤖 BoardHub
[🔗 English README](https://github.com/Kyabc/BoardHub/blob/main/README.en.md)

Discord 上でボードゲームを遊ぶための Bot です。

現在は **ito** を遊べます。今後、対応ゲームを順次追加していく予定です。



---

# 👨‍💻 導入方法
Python や Docker 環境が無い方は[こちらのURL](https://discord.com/oauth2/authorize?client_id=1520256776392409230&permissions=563224861984832&integration_type=0&scope=bot)からbotを導入することも可能です。
⚠️ **注意**
本botは個人運営です。利用者が多くなると動作が重くなる場合があります。また、運営者の都合で予告なく公開を終了する可能性があります。長期的な運用や安定した稼働が必要な場合は、ご自身でホスティングすることをおすすめします。

## 必要環境
- Python (>=3.10)
  - uv
- Docker

## Python
```bash
$ uv sync
$ uv run python main.py
```

## Docker
```bash
$ docker build .
$ docker compose up
```

---

# 🎮️ 遊べるゲーム

## ito
「ito」は、プレイヤー全員で数字カードを小さい順に並べる協力型の会話ゲームです。
### コマンド一覧
- **`/ito create`**
  - ゲームを作成します
- **`/ito join`**
  - ゲームに参加します
- **`/ito leave`**
  - ゲームから退出します
- **`/ito state`**
  - 現在の参加者を確認します
- **`/ito start [topic]`**
  - ゲームを開始します。
  - `topic` は省略可能です
  - 指定した場合はそのお題で開始します
  - 指定しない場合はランダムなお題が選ばれます
  - 参加者全員に DM で数字カードが配布されます
- **`/ito open-cards`**
  - 全プレイヤーの数字カードを公開します
- **`/ito end`**
  - 現在のゲームを終了します
- **`/ito kick @user`**
  - 指定したプレイヤーをゲームから除外します
- **`/ito help`**
  - コマンド一覧を表示します

### 遊び方
1. `/ito create` でゲームを作成
2. 各プレイヤーが `/ito join` で参加
3. `/ito start` でゲーム開始
4. DM で自分の数字カードとお題を確認
5. お題に沿って会話しながら順番を推理
6. `/ito open-cards` で答え合わせ
7. 続ける場合は再度 `/ito start`、終了する場合は `/ito end`

### お題について
Bot にはあらかじめ複数のお題が登録されています。ゲーム開始時にお題を指定しない場合は、登録された中からランダムなお題が選択されます。
`/ito start [topic]` を使うことで、自由にお題を指定することもできます。
#### お題を自分で設定する場合のコマンド例
```text
/ito start 行きたい旅行先
/ito start 白米に合うもの
/ito start 神様も引きそうなお願い
```

#### 注意事項
- 登録されているお題は AI を利用して生成しています。
- AI 生成のお題は内容や難易度にばらつきがある場合があります。

---


# 📨 連絡先

不具合報告や機能要望、その他お問い合わせは [terry (@terrytwitch)](https://x.com/terrytwitch) までお願いします。
