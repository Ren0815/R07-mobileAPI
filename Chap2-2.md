# Flutterの授業で学んだことまとめ
## プログラムの基本
#### StatefulWidgetクラス
動的、操作して表示が変わる  
状態を扱うためのStateクラスを持つ  
ステートが更新されるたびにbuildが呼び出される
```

  void _setMessage() {
    setState(() {
      _message = 'タップしました！';
    });
  }
```
setState ステートの更新をステートクラスに知らせる  
```
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: Text(widget.title)),
      body: Text(_message, style: TextStyle(fontSize: 32.0)),
      floatingActionButton: FloatingActionButton(
        onPressed: _setMessage,
        tooltip: 'set message.',
        child: Icon(Icons.star),
      ),
    );
  }
```
ボタンが押されたらメッセージを更新、更新されたステートにしたがってアプリバーのテキストも更新される

#### 複雑なクラス
Dataクラス
```
class Data{
  int_price;
  String_name;

  Data(this.name, this.price): super();
  @override
  String toString(){
    return _name + ':' + _price.toString() + '円';
  }
}
```
引数で受け取った値のnameとpriceを文字型にして出力

Dataインスタンス
```
static final _data = [
  Data('Apple',200),
  Data('Orange',150),
  Data('Peach',300)
];
Data _item;
```
呼び出されるデータのリストの用意
リストの最初の項目に_itemを設定することで起動時に最初のDataが表示される

_setData
```
void_setData(){
  setState((){
    _item = (_data..shuffle()).first;
  });
}
```
shuffleでリストの順番をランダムに入れ替え