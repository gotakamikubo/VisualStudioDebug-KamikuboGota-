# Visual Studio Debug Report

## ブレークポイント

![k](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/BreakPoint.gif)
コード行の左にある余白をクリックする,`F9`を押すことでブレイクポイントを設定できます。

`F5`を押す ([デバッグ]→[デバッグの開始] の順に選択する) か、デバッグ ツールバーの [デバッグの開始] ボタンを選択すると、デバッガーが最初のブレークポイントで実行されます。<br>
 アプリがまだ実行されていない場合、`F5`を押すとデバッガーが起動し、最初のブレークポイントで停止する。

 ブレークポイントは、Visual Studio が実行コードを中断する場所を示している。<br>
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
関数の中にまで進んでいくので、詳しくプログラムの動きを理解するために使われる。

### Step out

![step out](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/Step_Out.gif)
