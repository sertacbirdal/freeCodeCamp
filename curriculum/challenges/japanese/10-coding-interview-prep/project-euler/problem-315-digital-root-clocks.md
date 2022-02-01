---
id: 5900f4a71000cf542c50ffba
title: '問題 315: 数字根時計'
challengeType: 5
forumTopicId: 301971
dashedName: problem-315-digital-root-clocks
---

# --description--

<img class="img-responsive center-block" alt="137 から始まり数字根を計算する、サムとマックスの時計のアニメーション" src="https://cdn.freecodecamp.org/curriculum/project-euler/digital-root-clocks.gif" style="background-color: white; padding: 10px;" />

サムとマックスは、2 台のデジタル時計を数字根時計に作り変えるよう頼まれました。

数字根時計とは、数字根を 1 ステップずつ計算するデジタル時計です。

数字が入力されると、時計はその数字を表示してから計算を開始し、結果が出るまでの中間値をすべて表示します。 例えば数字 137 が入力されると、`137` → `11` → `2` と表示した後、表示を消して次の数字を待ちます。

各デジタル数字を構成する発光セグメントは、横方向に 3 本 (上、中、下) と縦方向に 4 本 (左上、右上、左下、右下) あります。 数字 `1` は右上と右下の縦セグメント、数字 `4` は中央の横セグメントと、左上、右上、右下の縦セグメントで作られます。 数字 `8` では全セグメントが点灯します。

この時計は、セグメントを点灯 / 消灯させたときのみエネルギーを消費します。 `2` を点灯させるには 5 回の遷移が必要ですが、`7` では 4 回しか遷移しません。

サムとマックスはそれぞれ異なる時計を作りました。

サムの時計に例えば 137 が入力されると、時計は `137` を表示した後、表示を消し、次の数字 (`11`) を表示し、再び表示を消し、最終的に最後の数字 (`2`) を表示し、しばらくすると消えます。

この例 (数字 137) では、サムの時計は次のように遷移します。

- `137`: $(2 + 5 + 4) × 2 = 22$ 回の遷移 (`137` の点灯と消灯)
- `11`: $(2 + 2) × 2 = 8$ 回の遷移 (`11` の点灯と消灯)
- `2`: $(5) × 2 = 10$ 回の遷移 (`2` の点灯と消灯)

計 40 回の遷移があります。

マックスの時計は、これとは違う動きをします。 パネル全体を消灯するのではなく、次の数に必要のないセグメントのみを消灯するという賢い方法です。

137 の場合、マックスの時計は次のように遷移します。

- `137`: $(2 + 5 + 4) × 2 = 11$ 回の遷移 (`137` の点灯)、$7$ 回の遷移 (`11` に不要なセグメントを消灯)
- `11` : $0$ 回の遷移 (数字 `11` は正しく点灯済み)、$3$ 回の遷移 (1 つ目の `1` と、2 つ目の `1` の下部を消灯、上部は数字 `2` と共通)
- `2` : $4$ 回の遷移 (`2` を作るために残りのセグメントを点灯)、$5$ 回の遷移 (数字 `2` を消灯)

計 30 回の遷移があります。

当然ながら、マックスの時計はサムの時計よりも消費電力が少なくなります。 2 台の時計に、$A = {10}^7$ から $B = 2 × {10}^7$ までの全素数を入力します。 サムの時計で必要な遷移の総数と、マックスの時計で必要な遷移の総数との差を求めなさい。

# --hints--

`digitalRootClocks()` は `13625242` を返す必要があります。

```js
assert.strictEqual(digitalRootClocks(), 13625242);
```

# --seed--

## --seed-contents--

```js
function digitalRootClocks() {

  return true;
}

digitalRootClocks();
```

# --solutions--

```js
// solution required
```