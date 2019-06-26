# Visual Studio Debug Report

## ブレイクポイント

![k](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/BreakPoint.gif)
コード行の左にある余白をクリックすることでブレイクポイントを設定できます。

F5 キーを押す ([デバッグ]→[デバッグの開始] の順に選択する) か、デバッグ ツールバーの [デバッグの開始] ボタンを選択すると、デバッガーが最初のブレークポイントで実行されます。<br>
 アプリがまだ実行されていない場合、F5 キーを押すとデバッガーが起動し、最初のブレークポイントで停止します。

 ブレークポイントは、Visual Studio が実行コードを中断する場所を示している。<br>
これにより、変数の値またはメモリの動作を確認したり、コードの分岐が実行されるかどうかを確認したりすることができる。<br>
基礎的なデバッグ。

## Step over/in/out

### Step over

![step over](https://raw.github.com/wiki/gotakamikubo/VisualStudioDebug-KamikuboGota-/images/Step_over.gif)

デバッグ中にF10 を押す ([デバッグ]→[ステップ オーバー] の順に選択する)ことでアプリ コード内の関数またはメソッドにステップ インすることなく、デバッガーが進められる(コードはまだ実行されている)。<br>
 Step overによって、関心のないコードをスキップすることで目的のコードまですばやく到達できる、プログラムの全体的な流れを確認するときに使用されます。