# 终端APP接口文档

### 1.概述


将主页主体分为五块。分别对应后录2.1至2.3。详情见后录。

![1](https://i.loli.net/2019/04/10/5caddf710200b.png)



### 2.详细接口

所有接口返回数据都按以下格式为基础。
data实际内容对应后录每章的响应体

|  | RESULTCODE | DATA | MSG |
|  :-:  | :-: | :-: | :-: | :-: |
| 类型 | int  | array | String |
| 说明 | 0成功 | \ | 错误信息 |


#### 2.1 横滚轮播图片

**Http-Get-Json**

请求: url/../(具体接口地址不做要求)

响应体:

|   | url  | title | 
| :-: | :-: | :-: |
| 类型 | String | String  | 
| 说明 | 图片的网络路径  | 标题 |

示例:

```
{
    "RESULTCODE": 0,
    "MSG": "",
    "DATA":  [
        {
            "url": "xxx/1.png",
            "title": "标题1"
        },
        {
            "url": "xxx/2.png",
            "title": "标题2"
        }
    ],
}
```


#### 2.2 党建动态、政策文件、基层党建

**Http-Get-Json**

党建动态、政策文件、基层党建整体一致，所以使用相同的结构。


响应体:

|   | url  | title | time | img |
| :-: | :-: | :-: | :-: | :-: |
| 类型 | String | String | String | String |
| 说明 | 网页地址  | 标题 | 发布时间 | 若存在>=1图片则附上第一张图片url,若无就用null |

示例:

```
{
    "RESULTCODE": 0,
    "MSG": "",
    "DATA": [
        {
            "url": "xxxxx",
            "title": "标题1",
            "time":"2018年10月2日",
            "img":"xxx/1.png"
        },
        {
            "url": "xxxxx",
            "title": "标题2",
            "time":"2018年10月2日",
            "img":"xxx/1.png"
        }
    ],
}
```


#### 2.3 党建期刊

**Http-Get-Json**

响应体:


|   | url  | title | content |
| :-: | :-: | :-: | :-: |
| 类型 | String | String | object | 
| 说明 | 封面图片网址  | 标题 | 期刊内容 |

**content:**

|   | imgs  | title | 
| :-: | :-: | :-: |
| 类型 | array | String  | 
| 说明 | 数组-但里面全部都是图片网络路径  | 子标题 |


示例:

```
{
    "RESULTCODE": 0,
    "MSG": "",
    "DATA":  [
        {
            "url": "xxx/封面图片.png",
            "title": "标题1",
            "content": {
                "title": "子标题",
                "imgs": [
                    "xxx/期刊内容1.png",
                    "xxx/期刊内容2.png"
                ]
            }
        },
        {
            "url": "xxx/2.png",
            "title": "标题2"
        }
    ],
}
```

