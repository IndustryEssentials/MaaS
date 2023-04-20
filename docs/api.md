### API 接口说明
- 协议：`HTTP`
- 方法：`POST`
- URL：`API管理`页面中`API`栏展示的内容。
- 请求内容格式：`multipart/form-data`
- 请求内容：`jpg`和`png`格式的图片。
- 应答内容格式：`application/json; charset=utf-8`
- 应答内容：
```
{
    "code": 0,
    "msg": "",
    "data": {
        "results": [
            {
                "class": 3,
                "class_name": "摩托车",
                "confidence": 0.8,
                "rect": {
                    "left": 100,
                    "top": 100,
                    "width": 200,
                    "height": 100
                }
            }
        ]
    }
}
```
说明：

  - `code`: `0`表示成功，其他表示失败。
  - `msg`: 失败时的错误消息。
  - `data`: 成功时的数据。
  - `results`: 推理结果，列表类型。
  - `class`: 推理结果的原始值，对于检测算法，它表示某个类别。
  - `class_name`: 类别的名称。
  - `confidence`: 置信度。
  - `rect`: 矩形检测框。
  - `left`: 矩形检测框左上角的横坐标。
  - `top`: 矩形检测框左上角的纵坐标。
  - `width`: 矩形检测框的宽度。
  - `height`: 矩形检测框的高度。

### curl 调用示例
假设`URL`为`http://192.168.0.100:8220/model-master/api/v1/infer-apis/ren-che-fei`，推理的图片路径为`D:/img001.jpeg`，则`curl`调用`API`的命令如下。
```
curl -X POST 'http://192.168.0.100:8220/model-master/api/v1/infer-apis/ren-che-fei' --form 'file=@"/D:/img001.jpg"'
```
