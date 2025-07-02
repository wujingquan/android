```
@Composable
fun RememberPasswordRow() {
    var checked by remember { mutableStateOf(false) }

    Row(
        modifier = Modifier
            .clickable { checked = !checked }
            .padding(8.dp),
        verticalAlignment = Alignment.CenterVertically
    ) {
        Checkbox(
            checked = checked,
            onCheckedChange = null // 让Checkbox变为只读，交互交给Row
        )
        Text("记住密码")
    }
}
```

- Checkbox默认有边距，可以通过width和height来限制，20dp
- 当`onCheckedChange=null`时，Checkbox变为只读，此时它没有了边距，与Text组件没有间隙

```
Row(
      verticalAlignment = Alignment.CenterVertically
    ) {
      Checkbox(
        checked = checked,
        onCheckedChange = { checked = it },
        modifier = Modifier.height(20.dp).width(20.dp).background(Color.Black).padding(all = 0.dp)
      )
      Text("忘记密码")
    }
```

