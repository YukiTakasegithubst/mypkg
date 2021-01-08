# mypkg

## ロボットシステム課題2

### ROSでのTopic通信の課題

#### 必要なもの

- Ubuntu20.04
- Raspberry Pi 4

#### 通信のやり方

ROSのインストールが必要  

terminalの一つで```roscore```を実行しておく

count.pyの通信を行いたいとき

```ls -l count.py```  
```chmod +x count.py```  
```rosrun mypkg count.py```

この時新しく文が出てこなければ準備OK

twice.pyの通信を行いたいとき

```chmod +x twice.py```  
```rosrun mypkg twice.py```

この時新しく文が出てこなければ準備OK

#### 通信状態の確認法

通信ができていれば以下のコードを実行した際、動作しているファイル名が表示される

```rosnode list```  
```rostopic list```

通信中に以下のコードを実行すれば数字が出続ける

count.pyの場合  
```rostopic echo /count_up```

twice.pyの場合  
```rostopic echo /twice```
