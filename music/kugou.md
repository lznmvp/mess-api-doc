#酷狗音乐

## 获取音乐详情

接口地址: `kugou/song`

请求示例: `kugou/song?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|无|

## 获取音乐播放地址

接口地址: `kugou/url`

请求示例: `kugou/url?id=xxxx&quality=128`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|无|
|quality|√|音质||

说明: 码率类型：128 192 320

## 获取音乐歌词

接口地址: `kugou/lrc`

请求示例: `kugou/lrc?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|默认获取翻译歌词|

## 获取音乐图片

接口地址: `kugou/pic`

请求示例: `kugou/pic?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID||

## 获取专辑详情

接口地址: `kugou/album`

请求示例: `kugou/album?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|专辑ID|无|

## 音乐歌单

说明：获取歌单中的所有音乐

接口地址: `kugou/songList`

请求示例: `kugou/songList?id=xxxx&pageSize=100&page=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|歌单的ID|无|

## 搜索

说明：搜索关键词可以搜索 音乐 / 歌手 / 专辑 / 歌单 / 视频 / 电台 / 用户 / 歌词

当前支持类型 `song singer album songList video radio user lrc`

接口地址: `kugou/search`

请求示例: `kugou/search?s=xxxx&type=song&pageSize=100&page=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|s|×|搜索关键词|详细见下面说明|
|type|×|搜索类型|默认为 song|
|pageSize|×|请求数量|默认为30|
|page|×|分页|默认第0页|


## 获取MV信息

接口地址: `kugou/mv`

请求示例: `kugou/mv?id=xxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MV ID||

## 获取MV播放地址

接口地址: `kugou/mvUrl`

请求示例: `kugou/mvUrl?id=xxxx&quality=1080`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MVID||
|quality|×|视频格式|默认480 |

说明: 视频大小类型：1080 720 480 240
