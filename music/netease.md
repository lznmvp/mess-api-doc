#网易云音乐

## 音乐详情

接口地址: `netease/song`

请求示例: `netease/song?id=xxxx,xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID,可一次获取多首音乐信息,必须使用英文逗号分开|无|

## 音乐播放地址

接口地址: `netease/url`

请求示例: `netease/url?id=xxxx&quality=192000`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|无|
|quality|√|音质 如果最大音质获取出错则自动转其他音质|默认320000 |

说明: 码率类型：128000 192000 320000 999000

## 音乐歌词

接口地址: `netease/lrc`

请求示例: `netease/lrc?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|默认获取翻译歌词|

## 音乐图片

接口地址: `netease/pic`

请求示例: `netease/pic?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID||
|imgSize|√|音乐ID|默认获取200x200大小的图片 其他大小自行尝试|

## 专辑详情

接口地址: `netease/album`

请求示例: `netease/album?id=xxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|专辑ID|无|

## 音乐歌单

说明：获取歌单中的所有音乐

接口地址: `netease/songList`

请求示例: `netease/songList?id=xxxx&limit=100`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|网易云歌单的ID|无|

由于网易云接口本身不支持分页，固定位每次请求1000条,超出1000首歌的歌单无法获取完整歌单

## 搜索

说明：搜索关键词可以搜索 音乐 / 歌手 / 专辑 / 歌单 / 视频 / 电台 / 用户 / 歌词

当前支持类型 `song singer album songList video radio user lrc`

接口地址: `netease/search`

请求示例: `netease/search?s=xxx&type=song&limit=100&offset=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|s|×|搜索关键词|详细见下面说明|
|type|×|搜索类型|默认为 song|
|pageSize|×|请求数量|默认为30|
|page|×|分页|默认第0页|


## 歌单分类

接口地址: `netease/songList/category`

请求示例: `netease/songList/category`


## 精品歌单

接口地址: `netease/songList/highQuality`

请求示例: `netease/songList/highQuality?cat=全部&limit=100`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|categoryType|×|歌单分类|默认全部|
|orderType|×|分别对应最新和最热| 可选值为 'new' 和 'hot',默认为 'hot'|
|pageSize|×|获取条数|默认30 |
|lasttime|×|上次返回的结果的lasttime值|


## 热门歌单

接口地址: `netease/songList/hot`

请求示例: `netease/songList/hot?cat=全部&limit=100&offset=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|categoryType|×|歌单分类|默认全部|
|orderType|×|分别对应最新和最热| 可选值为 'new' 和 'hot',默认为 'hot'|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 用户歌单信息

接口地址:`netease/songList/user`

请求示例: `netease/songList/user?uid=xxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|uid|√|用户ID|用户ID|

## MV信息

接口地址: `netease/mv`

请求示例: `netease/mv?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MV ID||

## MV播放地址

接口地址: `netease/mvUrl`

请求示例: `netease/mvUrl?id=xxxx&quality=1080`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MVID||
|quality|×|视频格式|默认480 |

说明: 视频大小类型：1080 720 480 240

## MV排行榜

接口地址: `netease/mvList/top`

请求示例: `netease/mvList/top?limit=10&offset=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 歌手信息

接口地址: `netease/artist/info`

请求示例: `netease/artist/info?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||



## 歌手排行榜

接口地址: `netease/artist/top`

请求示例: `netease/artist/top?page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|


## 歌手歌曲

接口地址: `netease/song/artist`

请求示例: `netease/song/artist?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||

## 歌手专辑

接口地址: `netease/album/artist`

请求示例: `netease/album/artist?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||


## 歌手MV

接口地址: `netease/mv/artist`

请求示例: `netease/mv/artist?id=xxxxxx`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌手ID||


## 最新音乐

接口地址: `netease/song/new`

请求示例: `netease/song/new`


## 最新专辑

接口地址: `netease/album/new`

请求示例: `netease/album/new`

## 音乐评论

接口地址: `netease/comment/song`

请求示例: `netease/comment/song?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌曲ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 专辑评论

接口地址: `netease/comment/album`

请求示例: `netease/comment/album?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|专辑ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## MV评论

接口地址: `netease/comment/mv`

请求示例: `netease/comment/mv?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|MV ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## Video评论

接口地址: `netease/comment/video`

请求示例: `netease/comment/video?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|Video ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 歌单评论

接口地址: `netease/comment/songList`

请求示例: `netease/comment/songList?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌单ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 音乐热门评论

接口地址: `netease/comment/song/hot`

请求示例: `netease/comment/song/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌曲ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 专辑热门评论

接口地址: `netease/comment/album/hot`

请求示例: `netease/comment/album/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|专辑ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## MV热门评论

接口地址: `netease/comment/mv/hot`

请求示例: `netease/comment/mv/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|MV ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## Video热门评论

接口地址: `netease/comment/video/hot`

请求示例: `netease/comment/video/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|Video ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 歌单热门评论

接口地址: `netease/comment/songList/hot`

请求示例: `netease/comment/songList/hot?id=xxxx&page=0&pageSize=30`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|×|歌单ID||
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|