表单
```html
<form>
    First Name:<br />
    <input type="text" name="firstname" />
    <br />
    Last Name:<br />
    <input type="text" name="lastname" />
    <br />
    <input type="radio" name="sex" value="male" />Male
    <input type="radio" name="sex" value="female" />Femal
    <br />
    <input type="submit" value="Submit" />
</form>
```

###### form 属性
| 属性           | 值  | 描述                | 示例                     |
| -------------- | --- | ------------------- | ------------------------ |
| action         | URL | 提交表单的地址      | action="action_page.php" |
| method         | GET | HTTP方法（默认GET） | method="GET"             |
| target         |     |                     |                          |
| accept-charset |     |                     |                          |
###### input 属性
| 属性  | 值                | 描述                         | 示例        |
| ----- | ----------------- | ---------------------------- | ----------- |
| type  | text,radio,submit | 文本输入，单选按钮，提交按钮 | type="text" |
| name  | 文本              | 该项的名称                   |             |
| value | 文本              | 该项的值                     |             |

<form>
    First Name:<br />
    <input type="text" name="firstname" />
    <br />
    Last Name:<br />
    <input type="text" name="lastname" />
    <br />
    <input type="radio" name="sex" value="male" />Male
    <input type="radio" name="sex" value="female" />Femal
    <br />
    <input type="submit" value="Submit" />
</form>
