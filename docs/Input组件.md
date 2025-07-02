```
Column(
    modifier = Modifier.fillMaxSize(),
    horizontalAlignment = Alignment.CenterHorizontally,
    verticalArrangement = Arrangement.Center
  ) {

    Row{
      Text("您好，哈哈哈")
      Text("欢迎来到我的智能家居系统132！")
    }
    Row() {
      Text("用户名")
      TextField(value = "", onValueChange = {str -> Log.e("test", str)})
    }
    Row() {
      Text("密码")
      TextField(value = "", onValueChange = {str -> Log.e("test", str)})
    }
    TextButton(onClick = {Log.e("test", "登录")}) {
      Text("登录")
    }
  }
```

