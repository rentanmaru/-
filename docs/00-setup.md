# 00 環境構築と Git 早見表

## 1. 確認済みの環境（2026-09-06 時点）

| ツール | バージョン | 用途 |
|---|---|---|
| Node.js | v24.15.0 | JavaScript をブラウザなしで実行する |
| npm | 11.12.1 | ライブラリの取得（Node に同梱） |
| git | 2.54 | 変更履歴の管理 |
| VS Code | インストール済み | エディタ |

確認コマンド（PowerShell でもターミナルでも同じ）:

```bash
node --version
npm --version
git --version
```

## 2. VS Code 拡張機能

VS Code 左端の四角いアイコン（拡張機能）で検索して入れる。

| 拡張名 | 何をしてくれるか |
|---|---|
| Japanese Language Pack for VS Code | メニューを日本語化 |
| ESLint | JavaScript の書き間違い・悪い書き方を赤線で教える |
| Prettier - Code formatter | 保存時にインデントや改行を自動で整える |
| Live Server | HTML を右クリック → ブラウザで開き、保存すると自動リロード |

Prettier を「保存時に自動整形」にする設定:
`Ctrl + ,` で設定を開き、「format on save」で検索してチェックを入れる。

## 3. Git の初期設定（最初の 1 回だけ）

```bash
git config --global user.name "自分の名前（ローマ字でも可）"
git config --global user.email "GitHub に登録するメールアドレス"
```

確認:

```bash
git config --global --list
```

## 4. Git コマンド早見表

Git は「セーブポイントを作る道具」。Unity でいえばシーンをバージョン付きで保存していくイメージ。

| やりたいこと | コマンド | メモ |
|---|---|---|
| このフォルダを Git 管理にする | `git init` | 最初の 1 回だけ |
| 今の状態を見る | `git status` | 迷ったらまずこれ |
| 変更をセーブ候補に入れる | `git add ファイル名` / `git add .` | `.` は全部 |
| セーブする（コミット） | `git commit -m "メッセージ"` | メッセージは「何をしたか」を日本語で OK |
| 履歴を見る | `git log --oneline` | 1 行ずつ表示 |
| 差分を見る | `git diff` | add する前の変更 |
| 新しいブランチを作って移動 | `git switch -c ブランチ名` | 実験用の分岐 |
| ブランチを移動 | `git switch main` | |
| ブランチ一覧 | `git branch` | `*` が今いる場所 |
| GitHub に送る | `git push` | 初回は `git push -u origin main` |
| GitHub から取ってくる | `git clone URL` | 別 PC で作業するとき |

コミットメッセージの例:

```
数当てゲームの雛形を作成
ToDo の削除ボタンを実装
localStorage への保存を追加
```

## 5. GitHub への公開手順（自分で行う）

1. https://github.com でアカウントを作成する（メール・パスワードは自分で入力）
2. 右上「+」→「New repository」→ 名前は `js-learning` など → Public → Create
3. 表示される「…or push an existing repository」の 3 行をターミナルにコピーして実行

```bash
git remote add origin https://github.com/ユーザー名/js-learning.git
git branch -M main
git push -u origin main
```

4. 初回は GitHub のログイン画面がブラウザで開くので、自分でログインする
5. 2 回目以降は `git push` だけで送れる

## 6. よく出るエラーと読み方

| エラー文 | 意味 | 対処 |
|---|---|---|
| `nothing to commit, working tree clean` | 変更がない | エラーではない。正常 |
| `fatal: not a git repository` | Git 管理外のフォルダにいる | `cd` で正しいフォルダに移動 |
| `Please tell me who you are` | 名前・メール未設定 | 上の 3 章を実行 |
| `rejected ... fetch first` | GitHub 側に自分の PC にない変更がある | `git pull` してから `git push` |

## 7. Node で JavaScript を実行する

```bash
node ファイル名.js
```

例: `00-setup` フォルダで `node hello.js`。
ターミナルの現在地は `pwd`（Git Bash）または `Get-Location`（PowerShell）で確認できる。
