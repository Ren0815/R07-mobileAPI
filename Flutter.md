# Flutterの授業で学んだことまとめ
## git
#### ファイルのアップロード
ソース管理→変更をステージ  
コメントを書きコミット  
ここまででローカルに保存  
ソース管理の右にある三点リーダーをクリックし、プッシュを選択することでアップロード完了  
**後からコミットに戻ることもできるのでコミット時のコメントは分かりやすく！**

## VScodeによる開発
コマンドパレットに'>Flutter: New Project'  
'Applification'を選択  
保存場所を選択  
プロジェクト名を入力

## プログラム
#### アプリ実行
```
void main(){
    runApp(ウィジェット);
}
```
mainが呼び出された際にrunAppが実行される  
runAppがアプリを起動する処理
#### StatelessWidgetクラス
ステート(状態を表す値)を持たないクラス  
```
class クラス名 extends StatelessWidget{
    
    @override
    Widget build(BuildContext context){
        return MaterialApp(略);
    }
}
```
build ウィジェットが生成される際に呼び出される  
return MaterialAppというクラスのインスタンスが返される  
build BuildContextというクラスのインスタンスが渡される
#### MaterialAppクラス
マテリアルデザインのアプリを管理するクラス　　
```
return MaterialApp(
    title: 'Flutter Demo',
    home: Text(
        'Hello,Flutter World!!',
        style: TextStyle(fontSize:32.0),
    ),
);
```
#### ScaffoldとAppBar
上部にアプリケーションバー、その下にテキストを表示する  
Scaffold　土台　AppBar　アプリケーションバー
```
home: Scaffold(
        appBar: AppBar(title: Text('Hello Flutter!')),
        body: Text('Hello Flutter World!!', style: TextStyle(fontSize: 32.0)),
      ),
    );
```
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