# Flutterの授業で学んだことまとめ
## アラートとダイアログ
# アラートの基本
showDialog
一時的にdialogを表示するメソッド  
AlertDialog
アラート表示をすることのできるdialog
```
showDialog(
    context: context,
    builder: (BuildContext context) => AlertDialog(
        title: Text("Hello!"),
        context: Text("This is sample"),
    )
);
```