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