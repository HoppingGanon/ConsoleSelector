
## Show-Console-Message
### 名前
Show-Console-Message
    
### 概要
Show-Console-Selectorのテーマに合わせたメッセージを表示できるコマンドレットです。
選択肢が必要ない場合などに利用してください。
    
    
### 構文
```
Show-Console-Message [[-Header] <String>] [[-Message] <String>] [[-Footer] <String>] [[-Title] <String>] [<CommonParameters>]
```

### パラメーター
```
-Header <String>
    選択肢の上部に表示するメッセージです。
    
-Message <String>
    主文として表示する文字列です。
    
-Footer <String>
    選択肢の下部に表示するメッセージです。
    
-Title <String>
    上部に表記するタイトルです。省略するとタイトルバーは表示しません。
```

### 例

```
PS C:\>Show-Console-Selector -Title 'テスト' -Header 'メッセージ' -Message 'これはテストです'

テスト
----------------------------------------------------------

メッセージ

これはテストです
```

## Show-Console-Selector

### 名前
Show-Console-Selector
    
### 概要
コンソール上で非常に可視的な選択肢を表示できるコマンドレットです。
画面は色分けされて表示されます。

### 構文
```
Show-Console-Selector [[-Header] <String>] [[-Model] <String[]>] [[-Footer] <String>] [[-Title] <String>] [-Help] [[-Default] <Int32>] [-Mult] [<CommonParameters>]
```

### パラメーター
```
-Header <String>
    選択肢の上部に表示するメッセージです。
    
-Model <String[]>
    選択肢として表示する文字列です。文字列配列を指定してください。
    
-Footer <String>
    選択肢の下部に表示するメッセージです。
    
-Title <String>
    上部に表記するタイトルです。省略するとタイトルバーは表示しません。
    
-Help [<SwitchParameter>]
    [Switch]指定すると操作方法が下部に表示されます。
    
-Default <Int32>
    初期状態のカーソル位置を設定できます。省略すると一番上に合わせます。
    
-Mult [<SwitchParameter>]
    [Switch]指定すると複数選択が可能になります。
```

### 例
```
PS C:\>Show-Console-Selector -Title 'テスト' -Header 'メッセージ' -Model @('はい', 'いいえ')

テスト
----------------------------------------------------------

メッセージ

    * はい
    * いいえ

----------------------------------------------------------
[↑/↓]カーソル移動 [Enter]決定 [BackSpace]戻る [Esc]終了

```

## Show-Console-FilePicker
### 名前
Show-Console-FilePicker

### 概要
コンソール上でファイルやフォルダを選択できる表示を行うコマンドレットです。

### 構文
Show-Console-FilePicker [[-Path] <String>] [[-Title] <String>] [-Help] [-Folder] [[-Extension] <Array>] [<CommonParameters>]

### パラメーター
```
-Path <String>
    初期表示するフォルダのパスです。省略するとカレントパスを開きます。
    
-Title <String>
    上部に表記するタイトルです。省略するとタイトルバーは表示しません。
    
-Help [<SwitchParameter>]
    [Switch]指定すると操作方法が下部に表示されます
    
-Folder [<SwitchParameter>]
    [Switch]指定するとフォルダのみ選択できるようになります。指定しない場合はファイルのみ選択できるようになります。
    
-Extension <Array>
    選択可能なファイル名をワイルドカードで指定します。
    
```

### 例
```
PS C:\>Show-Console-FilePicker (".\") -Folder

...

Name                           Value
----                           -----
Code                           0
Path                           {D:\Develop\}

```
