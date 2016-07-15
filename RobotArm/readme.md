# electron練習プログラム
node.js/socket.io/electron<br>
サーバーを立てないと動きません

# 内容物
* index.html
>GLSLもここに書いてある。canvasのidをmain.jsで取得し、GLで描画している。

* main.js
>GLのinitialize,描画や、アームが動くアルゴリズムなどなど。クライアント側のメイン

* minMatrix
>借り物。行列計算など

* ModelCreater.js
>3dモデル生成関数が入っている

* nodeMain.js
>サーバー側で動く。接続者情報とかアームの角度とかの情報を保持

* electronMain.js
>electronでexeを作るために使う

* bluetex.jpg , w089_03.jpg
>借り物。テクスチャに使う。スフィア環境mapping

* package.json
>install情報とか

* readme.md
>今開いてるやつ

# 利用手順

1. asarファイルを作る
> asar pack ./RobotArm .RobotArm.asar

2. パッケージしてexeを作る
> electron-packager ./ RobotArm --platform=darwin,win32 --arch=x64 --version=0.36.1

3. nodeでサーバーを立てる
> node nodeMain.js

4. exeを起動すると関節付きアームが表示される

5. スライダーを動かすとアームが動く

6. 他の接続者のアームにも動きが反映される

#