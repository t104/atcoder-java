# Java でファイルから標準入力を受け取る (VSCode)

使い方 (Windows, PowerShell)
1. [Java Extension Pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack) をインストールする。
1. a.java を開いて F5 で Launch Current File を実行する。
1. Integrated terminal が開いて a.in ファイルの 1 行目が表示されれば成功。

```
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

Try the new cross-platform PowerShell https://aka.ms/pscore6

PS E:\toshi\git\atcoder-java>  & 'c:\Users\toshi\.vscode\extensions\vscjava.vscode-java-debug-0.34.0\scripts\launcher.bat' 'C:\Program Files\AdoptOpenJDK\jdk-11.0.11.9-hotspot\bin\java.exe' '-agentlib:jdwp=transport=dt_socket,server=n,suspend=y,address=localhost:51352' '-Dfile.encoding=UTF-8' '-cp' 'C:\Users\toshi\AppData\Roaming\Code\User\workspaceStorage\e2fc0b34ced54ca254fbcc2296753ec9\redhat.java\jdt_ws\atcoder-java_e894e40a\bin' 'Solver' '^<' 'a.in'      
Input from java.
```

launch.json の args に設定するリダイレクトのための < を PowerShell では ^< にしないといけないことに注意  
[Debugger cannot read input file contents #667](https://github.com/microsoft/vscode-java-debug/issues/667)