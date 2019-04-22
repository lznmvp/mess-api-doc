## 1. 歌单获取

说明：获取歌单内容

接口地址: `music/netease/songList`

请求示例: `music/netease/songList?id=3778678&limit=100`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|网易云歌单的ID|无|

由于网易云接口本身不支持分页，固定位每次请求1000条,超出1000首歌的歌单无法获取完整歌单

## 2. 搜索音乐/专辑/歌词/歌单/MV/用户/歌手/电台搜索

说明：搜索关键词可以搜索音乐/歌手/专辑/歌单/视频/电台/用户/歌词

当前支持类型 `song singer album list video radio user lrc`

接口地址: `music/netease/search`

请求示例: `music/netease/search?key=579621905&s=我喜欢上你内心时的活动&type=song&limit=100&offset=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|s|×|搜索关键词|详细见下面说明|
|type|×|搜索类型|默认为 song|
|pageSize|×|请求数量|默认为30|
|page|×|分页|默认第0页|


## 3. 获取专辑详情

接口地址: `music/netease/album`

请求示例: `music/netease/album?key=579621905&id=32311`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|专辑ID|无|


## 4. 获取音乐详情

接口地址: `music/netease/song`

请求示例: `music/netease/song?key=579621905&id=526307800,526307800`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID,可一次获取多首音乐信息,必须使用英文逗号分开|无|

## 5. 获取音乐播放地址

接口地址: `music/netease/url`

请求示例: `music/netease/url?key=579621905&id=526307800&br=999000`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|无|
|quality|√|音质 如果最大音质获取出错则自动转其他音质|默认320000 |

说明: 码率类型：128000 192000 320000 999000

## 6. 获取音乐歌词

接口地址: `music/netease/lrc`

请求示例: `music/netease/lrc?key=579621905&id=526307800`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID|默认获取翻译歌词|

## 7. 获取音乐图片

接口地址: `music/netease/pic`

请求示例: `music/netease/pic?key=579621905&id=526307800`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|音乐ID||
|imgSize|√|音乐ID|默认获取200x200大小的图片 其他大小自行尝试|

## 8. 获取MV信息

接口地址: `music/netease/mv`

请求示例: `music/netease/mv?key=579621905&id=5965802`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MV ID||

## 9. 获取MV播放地址

接口地址: `music/netease/mvUrl`

请求示例: `music/netease/mvUrl?key=579621905&id=5965802&r=1080`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|id|√|MVID||
|qualityr|×|视频格式|默认480 |

说明: 视频大小类型：1080 720 480 240

## 10. 获取歌单分类

接口地址: `music/netease/songListCategory`

请求示例: `music/netease/songListCategory`


## 11. 获取精品歌单

接口地址: `music/netease/highQualitySongList`

请求示例: `music/netease/highQualitySongList?key=579621905&cat=全部&limit=100`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|categoryType|×|歌单分类|默认全部|
|orderType|×|分别对应最新和最热| 可选值为 'new' 和 'hot',默认为 'hot'|
|pageSize|×|获取条数|默认30 |
|lasttime|×|上次返回的结果的lasttime值|


## 12. 获取热门歌单

接口地址: `music/netease/hotSongList`

请求示例: `music/netease/hotSongList?key=579621905&cat=全部&limit=100&offset=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|categoryType|×|歌单分类|默认全部|
|orderType|×|分别对应最新和最热| 可选值为 'new' 和 'hot',默认为 'hot'|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 13. 获取MV排行榜

接口地址: `music/netease/topMvList`

请求示例: `music/netease/topMvList?key=579621905&limit=10&offset=0`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|pageSize|×|获取条数|默认30 |
|page|×|分页| 默认0|

## 14. 获取用户歌单信息

接口地址:`music/netease/userSongList`

请求示例: `music/netease/userSongList?key=579621905&uid=115119971`

|参数说明|是否必须|说明|默认值|
|------|-----|-----|---|
|uid|√|用户ID|用户ID|