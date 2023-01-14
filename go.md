# go

安装 **go编译器**，并验证：

```powershell
go version
```

安装 **go** 拓展、拓展包

新建 **test.go** 文件

```go
package main

import "fmt"

func main() {
    name := "Go Developers"
    fmt.Println("Azure for", name)
}
```

设置代理：

第一种：

```powershell
C:\> $env:GO111MODULE = "on"
C:\> $env:GOPROXY = "https://goproxy.cn"
```

第二种：

```txt
1. 打开“开始”并搜索“env”
2. 选择“编辑系统环境变量”
3. 点击“环境变量…”按钮
4. 在“<你的用户名> 的用户变量”章节下（上半部分）
5. 点击“新建…”按钮
6. 选择“变量名”输入框并输入“GO111MODULE”
7. 选择“变量值”输入框并输入“on”
8. 点击“确定”按钮
9. 点击“新建…”按钮
10. 选择“变量名”输入框并输入“GOPROXY”
11. 选择“变量值”输入框并输入“https://goproxy.cn”
12. 点击“确定”按钮
```

安装 第三方包

```txt
Ctrl+Shift+p
>>Go:Install/Update Tools
```

初始化 **go.mod**

```powershell
go mod init sample-app
```

点击 **侧边图标Run and Debug -> Run and Debug** 

在 **Debug console** 显示运行结果

在文件的右上角没有运行三角

官方式安装成功！

注：

如果想在文件右上角显示运行按钮，可在插件市场下载 **code runner** ,点击重新加载。

缺点：其他语言的项目如果使用 **code runner** 提供的运行方式，会导致中文乱码等。

建议：在进行其他语言的项目开发时，禁用此插件。