# Flutterの授業で学んだことまとめ
## プログラムの基本
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
