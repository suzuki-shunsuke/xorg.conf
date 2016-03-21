# xorg.conf

```
git clone git@github.com:suzuki-shunsuke/xorg.conf.git ~/.xorg
ln -s ~/.xorg/.Xdefaults ~/.Xdefaults
```

## ~/.Xdefaults

https://wiki.archlinuxjp.org/index.php/X_resources によると非推奨らしい(.Xresourcesを使えとのこと)。

## .Xresources

X クライアントアプリケーションの設定パラメータである X resources を設定

* ターミナルの色の定義
* ターミナルの設定
* DPI やアンチエイリアス、ヒンティングなど X フォントの設定
* X カーソルテーマの変更
* xscreensaver のテーマ設定
* ローレベルな X アプリケーションの設定 (xorg-xclock, xpdfAUR, rxvt-unicode など)

.Xresourcesを再読込するには

```
$ xrdb ~/.Xresources
```

## ~/.xprofile

https://wiki.archlinuxjp.org/index.php/Xprofile

* ウィンドウマネージャが起動する前に、X ユーザーセッションの初めにコマンドを実行
* ウィンドウを使うアプリケーションを起動するために使うことはできない
* .xinitrcと類似

## ~/.xinitrc

https://wiki.archlinuxjp.org/index.php/Xinitrc

* xinit や startx によって読み込まれるシェルスクリプト
* X サーバーが起動した時にデスクトップ環境やウィンドウマネージャなどのプログラムを起動するのに使われる(デーモンの起動や環境変数のセットなど)
