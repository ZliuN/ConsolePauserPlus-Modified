## ConsolePauserPlus-Modified
### 目前只有Windows下vscode的使用.
效果展示
![d6e5127674607ac9371e62c3bb71c08c.png](https://s2.loli.net/2024/12/04/k2uISYQjHGdAzc6.png)

基于[Dev-C++ 中 ConsolePauser.exe 的中文可替代版](https://github.com/xkk1/ConsolePauser)修改而来

配合vscode中的 [code runner](https://marketplace.visualstudio.com/items?itemName=formulahendry.code-runner) 插件实现

### 使用方法
在vscode-file-preferences-setting中搜索code-runner.executorMap

点击edit in settings.json

将c与cpp修改为
````
        "c": "cd $dir && gcc $fileName -o $fileNameWithoutExt  &&Pauser位置\\Pauser.exe $fileNameWithoutExt.exe input.txt",
        "cpp": "cd $dir && g++ $fileName -o $fileNameWithoutExt &&Pauser位置\\Pauser.exe $fileNameWithoutExt.exe input.txt",
````

随后在工作空间创建一个input.txt文件,将输入填到input.txt中,使用code runner运行程序即可.