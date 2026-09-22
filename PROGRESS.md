# 進捗チェックリスト

完了したら `[ ]` を `[x]` に変え、行末に一言メモ（学んだこと・詰まった点）を書く。
開始日: 2026-09-06

---

## フェーズ 0（第 1 週）環境構築・Git

合格基準: `git log` に自分のコミットがあり、GitHub 上でリポジトリが見える。

- [x] 0-1 VS Code 拡張を入れる（Japanese Language Pack / ESLint / Prettier / Live Server）
- [x] 0-2 `git config` で名前とメールを設定する
- [x] 0-3 `00-setup/hello.js` を自分で書いて `node hello.js` で実行する
- [x] 0-4 `git add` → `git commit` を自分の手で行う
- [ ] 0-5 GitHub アカウントを作り、このリポジトリを push する（自分で実施）
- [ ] 0-6 Git 練習: `branch` を切って変更し、`checkout` で戻り、`log` で確認する

## フェーズ 1（第 1〜4 週）JavaScript 基礎

合格基準: ToDo アプリがブラウザで動き、再読み込みしてもデータが残る。無補助チャレンジを 2 回連続ヒントなしで完了。

### 第 1 週
- [ ] 1-1 変数 `let` / `const`、数値・文字列・真偽値、`console.log`
- [ ] 1-2 条件分岐 `if` / `else`、比較演算子（`===` と `==` の違い）
- [ ] 1-3 ループ `while` / `for`
- [ ] 無補助チャレンジ①: 1〜100 の FizzBuzz を Node で書く

### 第 2 週
- [ ] 1-4 関数（宣言・式・アロー関数）、引数と戻り値、スコープ
- [ ] 1-5 配列（`push` / `length` / `includes` / `for...of`）
- [ ] 1-6 オブジェクト（プロパティの読み書き、ネスト）
- [ ] 作品①: 数当てゲーム（`01-js-basics/guess-game/`）
- [ ] 無補助チャレンジ②: 配列の合計・最大値・平均を返す関数を書く

### 第 3 週
- [ ] 1-7 HTML 最小限（`div` / `input` / `button` / `ul` / `li`、id と class）
- [ ] 1-8 CSS 最小限（セレクタ、色、余白、Flexbox）
- [ ] 1-9 DOM 操作（`querySelector` / `textContent` / `addEventListener`）
- [ ] 無補助チャレンジ③: ボタンを押すとカウントが増減するカウンターを作る

### 第 4 週
- [ ] 1-10 要素の生成と削除（`createElement` / `append` / `remove`）
- [ ] 1-11 `localStorage` と `JSON.stringify` / `JSON.parse`
- [ ] 作品②: ToDo アプリ（`01-js-basics/todo-app/`）追加・削除・完了切替・保存
- [ ] 無補助チャレンジ④: ToDo に「残り件数」表示を追加する

## フェーズ 2（第 5〜8 週）JavaScript 中級

合格基準: ポケモン図鑑で検索・エラー表示が動き、`npm run dev` で起動できる。`map` / `filter` / `async` を説明なしで使える。

### 第 5 週
- [ ] 2-1 配列メソッド `map` / `filter` / `find`
- [ ] 2-2 配列メソッド `reduce` / `forEach` / `sort`
- [ ] 2-3 分割代入・スプレッド構文・テンプレート文字列・オプショナルチェーン
- [ ] 無補助チャレンジ⑤: 商品リストから「在庫あり かつ 1000 円以下」の商品名一覧を作る

### 第 6 週
- [ ] 2-4 クラスと `this`（C# との違い）
- [ ] 2-5 ES Modules（`import` / `export`）でファイル分割
- [ ] 2-6 npm と `package.json`、Vite で開発サーバーを立てる
- [ ] 無補助チャレンジ⑥: ToDo アプリを `storage.js` / `ui.js` / `main.js` に分割する

### 第 7 週
- [ ] 2-7 `Promise` と非同期の考え方
- [ ] 2-8 `async` / `await`、`fetch`、`try` / `catch`
- [ ] 2-9 ESLint / Prettier の導入
- [ ] 無補助チャレンジ⑦: PokeAPI から任意のポケモン名を取得して `console.log` する

### 第 8 週
- [ ] 作品③: ポケモン図鑑（`02-js-intermediate/pokedex/`）検索・一覧・詳細・ローディング・エラー表示
- [ ] 無補助チャレンジ⑧: お気に入り機能を `localStorage` で追加する

## フェーズ 3（第 9〜11 週）TypeScript

合格基準: `tsc --noEmit` がエラー 0。`any` を使わずに移行できている。

### 第 9 週
- [ ] 3-1 `tsc` と `tsconfig.json`、Vite + TS テンプレート
- [ ] 3-2 基本型、配列・オブジェクトの型、`interface` と `type`
- [ ] 3-3 ユニオン型・リテラル型・`null` / `undefined` の扱い・型の絞り込み
- [ ] 無補助チャレンジ⑨: 渡された JSON に型を定義し、型エラーなく集計関数を書く

### 第 10 週
- [ ] 3-4 関数の型、ジェネリクス入門、`Partial` / `Pick` などユーティリティ型
- [ ] 3-5 API レスポンスに型を付ける
- [ ] 作品④: ポケモン図鑑を TypeScript に移行（`03-typescript/pokedex-ts/`）

### 第 11 週
- [ ] 作品⑤: タスク管理 CLI（`03-typescript/task-cli/`）型定義から設計する
- [ ] 無補助チャレンジ⑩: CLI に「期限順ソート」コマンドを追加する

## フェーズ 4（第 12〜16 週）React + TypeScript

合格基準: 最終作品が公開 URL で動き README が整っている。React + TS の ToDo をヒントなしで 1 から作れる。

### 第 12 週
- [ ] 4-1 Vite + React + TS の雛形、JSX、コンポーネントと props
- [ ] 4-2 `useState`、イベント、リスト表示と `key`、条件付きレンダリング
- [ ] 無補助チャレンジ⑪: カウンターとプロフィールカードを React で作る

### 第 13 週
- [ ] 4-3 `useEffect`、フォーム制御、`fetch` との組み合わせ
- [ ] 4-4 カスタムフック、コンポーネント分割、props の型付け
- [ ] 無補助チャレンジ⑫: ToDo アプリを React + TS で作り直す（`04-react-ts/todo-react/`）

### 第 14 週
- [ ] 4-5 `react-router` の基本（2〜3 画面）
- [ ] 最終作品 設計: 画面一覧・データ構造（型）・機能一覧を書き出す

### 第 15 週
- [ ] 最終作品 実装: 予約の追加・編集・削除、日付別一覧、`localStorage` 永続化

### 第 16 週
- [ ] 最終作品 仕上げ: カレンダー表示、バリデーション、デプロイ（GitHub Pages / Vercel）
- [ ] README 作成（概要・使用技術・工夫点・スクリーンショット・公開 URL）
- [ ] 発展（任意）: 保存先を Firebase Firestore に差し替える

## フェーズ 5（第 17 週〜・任意）応募準備

- [ ] Node.js + Express で最小 API を 1 本作る
- [ ] Next.js を 1 日触ってルーティングと SSR の概念を掴む
- [ ] GitHub プロフィール README を整える
- [ ] 応募書類の「制作物」欄の文章を書く
- [ ] 面接想定問答（なぜ JS/TS か・詰まったときの解決方法・作品の工夫点）
