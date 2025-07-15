# Flutterの授業で学んだことまとめ
## プログラムの基本
#### レイアウトを考える
部品を配置してレイアウトの作成、**ソースコードのコピー**ができるサイト
[Flutter studio](https://flutterstudio.app/)

| TextStyle |  |
|:---|:---|
|fontSize|フォントサイズ(double型)|
|fontWeight|フォントの太さ|
|fontFamily|フォントファミリー|
|fontStyle|フォントスタイル|
|color|テキスト色(ARGBカラー)|
```
style: TextStyle(fontSize:32.0,
color: const Color(0xff000000),
fontWeight: FontWeight.w700,
fontFamily: "Roboto"),
```
| 大まかなウィジェット |  |
|:---|:---|
|Center|中央ぞろえ|
|Container|コンテナ、他のウィジェットを格納しレイアウトなどを決める|

#### Container
コンテナ、他のウィジェットを格納しレイアウトなどを決める  
Edgeinsets
周囲の余白幅を設定する  
Alignment
配置場所を設定する  

#### Column,Row
複数のウィジェットを縦に並べて表示する  
mainAxisAlignment
ウィジェットが並ぶ方向  
crossAxisAlignment
ウィジェットに交差する方向  