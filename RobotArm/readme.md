#electron練習プログラム
node.js/socket.io/electron

#利用手順
asarファイルを作る
    asar pack ./RobotArm .RobotArm.asar
パッケージしてexeを作る
    electron-packager ./ RobotArm --platform=darwin,win32 --arch=x64 --version=0.36.1
nodeでサーバーを立てる
    node nodeMain.js
exeを起動すると関節付きアームが表示される
スライダーを動かすとアームが動く
他の接続者のアームにも動きが反映される

