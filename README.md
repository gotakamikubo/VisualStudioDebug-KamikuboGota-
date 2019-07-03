# Visual Studio Debug Report

## ブレークポイント

![k](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/BreakPoint.gif)
コード行の左にある余白をクリックする,`F9`を押すことでブレイクポイントを設定できます。

`F5`を押す ([デバッグ]→[デバッグの開始] の順に選択する) か、デバッグ ツールバーの [デバッグの開始] ボタンを選択すると、デバッガーが最初のブレークポイントで実行されます。<br>
 アプリがまだ実行されていない場合、`F5`を押すとデバッガーが起動し、最初のブレークポイントで停止する。
 ブレークポイントは、Visual Studio が実行コードを中断する場所を示している。<br>
ブレークポイントに右クリック→[条件]を押すことで条件を設定することができる。<br>
一時的にOFFにするなら `Ctrl + F9`、全てのブレークポイントを削除するならば `Shift + Ctrl + F9`を押す。<br>
変数の値またはメモリの動作を確認したり、コードの分岐が実行されるかどうかを確認したりすることができる基礎的なデバッグ。

## Step over/in/out

### Step over

![step over](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/Step_Over.gif)

デバッグ中にF10 を押す ([デバッグ]→[ステップ オーバー] の順に選択する)ことでアプリ コード内の関数またはメソッドにステップ インすることなく、デバッガーが進められる(コードはまだ実行されている)。<br>
 Step overによって、関心のないコードをスキップすることで目的のコードまですばやく到達する、プログラムの全体的な流れを確認するときに使用される。

***

### Step in

![step in](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/Step_In.gif)

デバッグ中に`F11`を押す（[デバッグ]→[ステップ イン]の順に選択する）ことでアプリの実行が 1 ステートメント進められる。<br>
`F5`でアプリを開始すると、デバッガーは実行される最初のステートメントで停止する。<br>
Step_Overとは違い、関数の中にまで進んでいくので詳しくプログラムの動きを理解するために使われる。

### Step out

![step out](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/Step_Out.gif)

Step_Outは上記2つに比べるとマイナーな部類に入る。<br>
デバッグ中に`shift + F11`を押すことで今実行している関数の外（呼び出し元）に出るまでプログラムを進める。<br>
関数の動作チェックができた時に呼び出し元に戻りたいときに使用される。

## 自動変数・ローカル変数ウィンドウ

### 自動変数ウィンドウ

![zidou](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/自動変数.png)

`Ctrl + Alt + V` → `A`の順に押す([デバッグ]→[ウィンドウ]→[自動変数]の順に選択する)ことで表示される。<br>
現在実行中の行に関係のある変数だけが表示される。<br>
変数に、新しい値や式を直接入力することができる。<br>
名前、値、および型の列に含まれるキーワードを検索することができ、`F3`を押すことで検索した変数が表示された場所まで移動する。<br>
変数に予想外の値が入力されていないかを調べたり、変数の値を変更することで正しくプログラムが動作するか調べるために使用される。

### ローカル変数ウィンドウ

![local](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/ローカルウィンドウ.png)

`Ctrl + Alt + V` → `L`の順に押す([デバッグ]→[ウィンドウ]→[ローカル]の順に選択する)ことで表示される。<br>
メソッド内限定の変数の内容が自動的に表示される。<br>
自動変数ウィンドウと同じく変数の値や式を直接入力、変数の検索ができる。<br>
変数の値が変更された時値が赤く表示されるので変数の値の監視がしやすく、
本来値が変更されないはずの変数の値が変更されていたとしても直ぐに確認できる。

## ウォッチ式

![wa](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/ウォッチ式.png)

`Ctrl + Alt + W` → `n(nは１～４までの数字)`の順に押す([デバッグ]→[ウィンドウ]→[ウォッチ]→[ウォッチ n(nは１～４までの数字) ]の順に選択する)ことで表示される。<br>
変数と式を常に監視する(対象外のときは淡色表示となる)。ウォッチ式は4つまで表示できる。<br>
[項目をウォッチに追加する]から、監視する変数、式を追加することができる。<br>
値が変更されると文字が赤く表示される。<br>
特定の変数の値だけを確認したいとき利用される。

## データブレイクポイント

![date1](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/データブレイクポイント２.png)

[デバッグ]→[ブレークポイントの作成]→[データブレイクポイント]の順に選択し、特定の変数のアドレス、バイト数、条件を入力。<br>
もしくは、自動変数・ローカル変数・ウォッチウィンドウのプロパティに右クリック→値が変更されたとき中断をクリックでデータブレイクポイントを設定。<br>
もし、条件を満たした場合下図のようになりプログラムが中断される。<br>

![date2](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/データブレイクポイント１.png)

データブレイクポイントは、変更されないはずの値が変更されていた場合や予想外の値になっていた場合などを見つけるときに使用される。

## メモリウィンドウ

![mem](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/メモリウィンドウ.png)

`Ctrl + Alt + M` → `n(nは１～４までの数字)`の順に押す([デバッグ]→[ウィンドウ]→[メモリ]→[メモリ n (nは１～４までの数字)]の順に選択する)ことで表示される。<br>
メモリウィンドウは4つまで表示できる。<br>
アドレス欄にアドレスを入れる、ポインタ、などを入力すれば該当アドレスのメモリーを直接確認することができるできる。<br>
メモリーの中身が変更されたとき、変更されたメモリーは赤色で表示される。<br>
メモリーにどのようにして割り当てられているかを確認するために使用される。

## コールスタック(呼び出し履歴)

![call](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/呼び出し.png)

