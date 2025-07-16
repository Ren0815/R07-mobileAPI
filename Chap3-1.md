# Flutterの授業で学んだことまとめ
## UIウィジェット
### ボタン・ウィジェットについて
#### TextButton
onPressed
ボタンが押されたときに実行されるメソッド  
child
ボタン内に表示されるウィジェット  
```
TextButton(
    onPressed: buttonPressed,
    child: Padding(
        padding: EdgeInsets.all(10.0),
        child: Text(
            "Push me!",
            style: TextStyle(略),
        )
    )
)
```

#### カスケード記法
(厳密には)式の値を元のオブジェクトにしたまま操作を行う記法  
同一のオブジェクトに対して複数の操作を行うことができる
```
void main(){
    test sample = test();

    sample.add(10);
    print(sample..add(4));
}
```

#### ユーザーからの入力のためのUI/Uｘ
TextField
自由に文字を入力させたいとき  
checkbox,Switch
要素に該当するかどうかチェックさせたいとき  
Radio,Dropdown
複数の要素から一つだけ選ばせたいとき  
Slider
特定の値の範囲で数値を入力させたいとき

#### if文を簡略化して書く
```
void main(){
    int a=10;
    print(a<10 ? "ok" : "ng");
}
```
判定式 ? tureの時の値 : falseの時の値
#### NULL
```
void checkChanged(bool? value){
    setState((){
        _checkded = value!;
        _selected = value ?? 'nodata';
    })
}
```
bool? value
NULL許容  
value!
非NULL保障  
value ?? 'nodata'
Nullの時の値