#QQ音乐

## 获取音乐详情

接口地址: `tencent/song`

请求示例: `tencent/song?id=xxxx,xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID,可一次获取多首音乐信息,必须使用英文逗号分开|无|

## 获取音乐播放地址

接口地址: `tencent/url`

请求示例: `tencent/url?id=xxxx&quality=128`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|无|
|quality|√|音质 如果最大音质获取出错则自动转其他音质|默认192 |

说明: 码率类型：24 96 128 192 320 ape flac

## 获取音乐歌词

接口地址: `tencent/lrc`

请求示例: `tencent/lrc?id=xxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|默认获取翻译歌词|

## 获取音乐图片

接口地址: `tencent/pic`

请求示例: `tencent/pic?id=xxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID||
|imgSize|√|音乐ID|默认获取200x200大小的图片 其他大小自行尝试|

## 获取专辑详情

接口地址: `tencent/album`

请求示例: `tencent/album?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|专辑ID|无|

## 音乐歌单

说明：获取歌单中的所有音乐

接口地址: `tencent/songList`

请求示例: `tencent/songList?id=xxxx&pageSize=100&page=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|歌单的ID|无|


## 搜索

说明：搜索关键词可以搜索 音乐 / 歌手 / 专辑 / 歌单 / 视频 / 电台 / 用户 / 歌词

当前支持类型 `song singer album songList video radio user lrc`

接口地址: `tencent/search`

请求示例: `tencent/search?keyword=xxxx&type=song&pageSize=100&page=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|keyword|×|搜索关键词|详细见下面说明|
|type|×|搜索类型|默认为 song|
|pageSize|×|请求数量|默认为30|
|page|×|分页|默认第0页|


## 歌单分类

接口地址: `tencent/songList/category`

请求示例: `tencent/songList/category`


## 热门歌单

接口地址: `tencent/songList/hot`

请求示例: `tencent/songList/hot?cat=全部&pageSize=100&page=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|categoryType|×|歌单分类|默认全部|
|orderType|×|分别对应最新和最热| 可选值为 'new' 和 'hot',默认为 'hot'|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 用户歌单信息

接口地址:`tencent/songList/user`

请求示例: `tencent/songList/user?uid=xxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|uid|√|用户ID|用户ID|

## 获取MV信息

接口地址: `tencent/mv`

请求示例: `tencent/mv?id=xxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MV ID||

## 获取MV播放地址

接口地址: `tencent/mvUrl`

请求示例: `tencent/mvUrl?id=xxxx&quality=1080`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MVID||
|quality|×|视频格式|默认480 |

说明: 视频大小类型：1080 720 480 240

## 歌单分类

接口地址: `tencent/mv/category`

请求示例: `tencent/mv/category`

## 热门MV

接口地址: `tencent/mv/hot`

请求示例: `tencent/mv/hot?&pageSize=100&page=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 歌手分类

接口地址: `tencent/artist/category`

请求示例: `tencent/artist/category`


## 歌手列表

接口地址: `tencent/artist/list`

请求示例: `tencent/artist/list?page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|


## 歌手音乐

接口地址: `tencent/song/artist`

请求示例: `tencent/song/artist?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||

## 歌手专辑

接口地址: `tencent/album/artist`

请求示例: `tencent/album/artist?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||


## 歌手MV

接口地址: `tencent/mv/artist`

请求示例: `tencent/mv/artist?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||


## 音乐评论

接口地址: `tencent/comment/song`

请求示例: `tencent/comment/song?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌曲ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 专辑评论

接口地址: `tencent/comment/album`

请求示例: `tencent/comment/album?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|专辑ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## MV评论

接口地址: `tencent/comment/mv`

请求示例: `tencent/comment/mv?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|MV ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 榜单评论

接口地址: `tencent/comment/top`

请求示例: `tencent/comment/top?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|榜单ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 歌单评论

接口地址: `tencent/comment/songList`

请求示例: `tencent/comment/songList?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌单ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 音乐热门评论

接口地址: `tencent/comment/song/hot`

请求示例: `tencent/comment/song/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌曲ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 专辑热门评论

接口地址: `tencent/comment/album/hot`

请求示例: `tencent/comment/album/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|专辑ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## MV热门评论

接口地址: `tencent/comment/mv/hot`

请求示例: `tencent/comment/mv/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|MV ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 榜单热门评论

接口地址: `tencent/comment/top/hot`

请求示例: `tencent/comment/top/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|榜单ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 歌单热门评论

接口地址: `tencent/comment/songList/hot`

请求示例: `tencent/comment/songList/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌单ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|