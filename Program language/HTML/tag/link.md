定义当前文档与外部资源之间的关系
#### Example
外部样式表
link to an external style sheet
```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="css/styles.css" />
    <link rel="icon" href="icon.ico" />
  </head>
  <body>
    <p>This paragraph is red</p>
  </body>
</html>
```
```css
/* css/style.css */
p{
  color: red;
  font-size: 16px;
}
```

#### Attributes
| Attribute | Value                                    | Description                                                                               |
| --------- | ---------------------------------------- | ----------------------------------------------------------------------------------------- |
| href      | URL                                      | Specifies the location of the linked document                                             |
| rel       | stylesheet, <br /> icon, <br /> prefetch | Required. Specifies the relationship between the current document and the linked document |
| sizes     | HeightxWidth                             | Specifies the size of the linked resource. Only for rel="icon"                            |
| title     |                                          | Defines a preferred or an alternate stylesheet                                            |
| type      | media_type                               | Specifies the media type of the linked document                                           |

#### Global Attributes
link tag supports the [Global Attributes in HTML](null)

#### Event Attributes
link tag supports the [Event Attributes in HTML](null)