#网易云音乐

## 音乐详情

接口地址: `netease/song`

请求示例: `netease/song?id=37239038,526307800`

| 参数说明 | 是否必须 | 说明                                                | 默认值 |
| -------- | -------- | --------------------------------------------------- | ------ |
| id       | √        | 音乐 ID,可一次获取多首音乐信息,必须使用英文逗号分开 | 无     |
| format   | X        | 格式化数据 1 格式化 0 不格式化                      | 0      |

```json
{
    "code": 200,
    "msg": "OK",
    "timestamp": 1556617619521,
    "data": {
        "privileges": [
            //数组 与songs中数组一一对应
            {
                "st": 0,
                "flag": 0,
                "subp": 1,
                "fl": 320000,
                "fee": 0,
                "dl": 320000,
                "cp": 1,
                "preSell": false,
                "cs": false,
                "toast": false,
                "maxbr": 999000, //当前音乐最大音质
                "id": 483258619, //音乐ID
                "pl": 320000,
                "sp": 7,
                "payed": 0
            }
        ],
        "code": 200,
        "songs": [
            {
                "no": 13,
                "copyright": 2,
                "fee": 0,
                "mst": 9,
                "pst": 0,
                "pop": 100,
                "dt": 128489,
                "rtype": 0,
                "s_id": 0,
                "rtUrls": [],
                "id": 483258619, //音乐ID
                "st": 0,
                "cd": "1",
                "publishTime": 1481290807500, //发布时间
                "cf": "",
                "h": {
                    "br": 320000, //极高音质
                    "fid": 0,
                    "size": 5141987, //音乐大小 单位B
                    "vd": -2
                },
                "mv": 0, // MV ID 若为0则无对应MV
                "al": {
                    "picUrl": "http://p2.music.126.net/OzLcwLmUSdoFvsxthLv3nA==/109951162820238045.jpg", //专辑图片
                    "name": "树深时见鹿dear的鬼畜歌~", //专辑名称
                    "tns": [],
                    "pic_str": "109951162820238045",
                    "id": 35035713, //专辑ID
                    "pic": 109951162820238045 //专辑图片ID
                },
                "l": {
                    "br": 128000, //标准音质
                    "fid": 0,
                    "size": 2056821, //音乐大小 单位B
                    "vd": -2
                },
                "m": {
                    "br": 192000, //较高音质
                    "fid": 0,
                    "size": 3085209, //音乐大小 单位B
                    "vd": -2
                },
                "cp": 0,
                "alia": [],
                "djId": 0,
                "ar": [
                    //歌手信息
                    {
                        "name": "树深时见鹿dear", // 歌手名称
                        "tns": [],
                        "alias": [],
                        "id": 12205587 //歌手ID
                    }
                ],
                "ftype": 0,
                "t": 0,
                "v": 11,
                "name": "【三国杀】这个rap有点带感" //歌曲名称
            }
        ]
    }
}
```

## 音乐播放地址

接口地址: `netease/url`

请求示例: `netease/url?id=37239038&quality=192000`

| 参数说明 | 是否必须 | 说明                                      | 默认值      |
| -------- | -------- | ----------------------------------------- | ----------- |
| id       | √        | 音乐 ID                                   | 无          |
| quality  | √        | 音质 如果最大音质获取出错则自动转其他音质 | 默认 320000 |

说明: 码率类型：128000 192000 320000 999000

## 音乐歌词

接口地址: `netease/lrc`

请求示例: `netease/lrc?id=37239038`

| 参数说明 | 是否必须 | 说明    | 默认值           |
| -------- | -------- | ------- | ---------------- |
| id       | √        | 音乐 ID | 默认获取翻译歌词 |

## 音乐图片

接口地址: `netease/pic`

请求示例: `netease/pic?id=37239038`

| 参数说明 | 是否必须 | 说明    | 默认值                                       |
| -------- | -------- | ------- | -------------------------------------------- |
| id       | √        | 音乐 ID |                                              |
| imgSize  | √        | 音乐 ID | 默认获取 200x200 大小的图片 其他大小自行尝试 |

## 专辑详情

接口地址: `netease/album`

请求示例: `netease/album?id=3159845`

| 参数说明 | 是否必须 | 说明                           | 默认值 |
| -------- | -------- | ------------------------------ | ------ |
| id       | √        | 专辑 ID                        | 无     |
| format   | X        | 格式化数据 1 格式化 0 不格式化 | 0      |

```json
{
    "code": 200,
    "msg": "OK",
    "timestamp": 1556618381899,
    "data": {
        "code": 200,
        "songs": [ // 专辑中的音乐列表
            {
                "no": 1,
                "fee": 0,
                "privilege": {
                    "st": 0,
                    "flag": 0,
                    "subp": 1,
                    "fl": 320000,
                    "fee": 0,
                    "dl": 320000,
                    "cp": 1,
                    "preSell": false,
                    "cs": false,
                    "toast": false,
                    "maxbr": 320000,
                    "id": 445886177,
                    "pl": 320000,
                    "sp": 7,
                    "payed": 0
                },
                "mst": 9,
                "pst": 0,
                "pop": 50,
                "dt": 249858,
                "rtype": 0,
                "rtUrls": [],
                "id": 445886177,// 音乐ID
                "st": 0,
                "cd": "1",
                "cf": "",
                "h": {
                    "br": 320000,
                    "fid": 18690598162123664,
                    "size": 10004942,
                    "vd": 2.58411
                },
                "mv": 0,
                "al": {
                    "picUrl": "http://p1.music.126.net/OzLcwLmUSdoFvsxthLv3nA==/109951162820238045.jpg", //专辑图片
                    "name": "树深时见鹿dear的鬼畜歌~",
                    "pic_str": "109951162820238045", //图片ID
                    "id": 35035713, //音乐所属专辑ID
                    "pic": 109951162820238050 //图片ID
                },
                "l": {
                    "br": 96000,
                    "fid": 18690598162123664,
                    "size": 3001514,
                    "vd": 2.4239
                },
                "cp": 0,
                "m": {
                    "br": 160000,
                    "fid": 18690598162123664,
                    "size": 5002494,
                    "vd": 2.96423
                },
                "djId": 0,
                "alia": [],
                "ar": [ // 歌手信息
                    {
                        "name": "树深时见鹿dear",//歌手名称
                        "id": 12205587 //歌手ID
                    }
                ],
                "ftype": 0,
                "t": 0,
                "v": 31,
                "name": "【不全明星】当你孤单你会想起谁" //音乐名称
            }
        ],
        "album": { // 专辑信息
            "artist": { 专辑主歌手
                "img1v1Url": "http://p1.music.126.net/VnZiScyynLG7atLIZ2YPkw==/18686200114669622.jpg",
                "picId_str": "109951162820236060",
                "musicSize": 10,
                "img1v1Id_str": "18686200114669622",
                "img1v1Id": 18686200114669624,
                "followed": false, // 是否关注该歌手
                "albumSize": 1,
                "picUrl": "http://p2.music.126.net/9Xz9eWM-q5lH1GXyQyLbGg==/109951162820236060.jpg", // 歌手图片
                "topicPerson": 0,
                "briefDesc": "",
                "name": "树深时见鹿dear", // 歌手名称
                "alias": [],
                "id": 12205587, // 歌手ID
                "picId": 109951162820236060,
                "trans": ""
            },
            "description": "我的鬼畜歌 选择部分传的 b站同网易云ID 有未收录的想听的欢迎私信 反正我看了也懒得传 2333", // 专辑描述
            "pic": 109951162820238050,
            "type": "专辑",
            "picUrl": "http://p2.music.126.net/OzLcwLmUSdoFvsxthLv3nA==/109951162820238045.jpg", //专辑图片
            "briefDesc": "我的鬼畜歌 选择部分传的 b站同网易云ID 有未收录的想听的欢迎私信 反正我看了也懒得传 2333",
            "artists": [ //专辑的歌手们
                {
                    "img1v1Url": "http://p1.music.126.net/VnZiScyynLG7atLIZ2YPkw==/18686200114669622.jpg",
                    "musicSize": 0,
                    "img1v1Id_str": "18686200114669622",
                    "img1v1Id": 18686200114669624,
                    "followed": false,
                    "albumSize": 0,
                    "picUrl": "http://p1.music.126.net/6y-UleORITEDbvrOLV0Q8A==/5639395138885805.jpg", //歌手图片
                    "topicPerson": 0,
                    "briefDesc": "",
                    "name": "树深时见鹿dear",
                    "alias": [],
                    "id": 12205587, //歌手ID
                    "picId": 0,
                    "trans": ""
                }
            ],
            "onSale": false,
            "alias": [],
            "id": 35035713, // 专辑ID
            "picId": 109951162820238050,
            "info": {  //评论信息
                "threadId": "R_AL_3_35035713", 
                "shareCount": 44,
                "resourceId": 35035713,
                "commentThread": {
                    "shareCount": 44,
                    "resourceId": 35035713,
                    "hotCount": 1,
                    "resourceTitle": "树深时见鹿dear的鬼畜歌~",
                    "resourceOwnerId": -1,
                    "id": "R_AL_3_35035713",
                    "likedCount": 0,
                    "resourceInfo": {
                        "imgUrl": "https://p2.music.126.net/OzLcwLmUSdoFvsxthLv3nA==/109951162820238045.jpg",
                        "name": "树深时见鹿dear的鬼畜歌~",
                        "id": 35035713,
                        "userId": -1
                    },
                    "resourceType": 3,
                    "commentCount": 48 //评论数量统计
                },
                "likedCount": 0,
                "liked": false,
                "resourceType": 3,
                "commentCount": 48 //评论数量统计
            },
            "publishTime": 1481290807500, //专辑发布时间
            "picId_str": "109951162820238045",
            "blurPicUrl": "http://p2.music.126.net/OzLcwLmUSdoFvsxthLv3nA==/109951162820238045.jpg", //缩略图
            "commentThreadId": "R_AL_3_35035713", //评论的ID信息
            "tags": "",
            "companyId": 0,
            "size": 10,
            "copyrightId": 0,
            "songs": [],
            "paid": false,
            "name": "树深时见鹿dear的鬼畜歌~", //专辑名称
            "subType": "录音室版", //专辑类型
            "status": 0
        }
    }
}
```

## 音乐歌单

说明：获取歌单中的所有音乐

接口地址: `netease/songList`

请求示例: `netease/songList?id=141998290&pageSize=20`

| 参数说明 | 是否必须 | 说明                           | 默认值 |
| -------- | -------- | ------------------------------ | ------ |
| id       | √        | 网易云歌单的 ID                | 无     |
| format   | X        | 格式化数据 1 格式化 0 不格式化 | 0      |

由于网易云接口本身不支持分页，固定位每次请求 1000 条,超出 1000 首歌的歌单无法获取完整歌单

```json
{
    "code": 200,
    "msg": "OK",
    "timestamp": 1557322797607,
    "data": {
        "privacy": 0,
        "trackNumberUpdateTime": 1546580252461, //歌单更新时间
        "subscribed": false, //是否关注
        "shareCount": 0, //分享次数
        "adType": 0, 
        "trackCount": 10, //音乐数量
        "specialType": 20, 
        "id": 2597018357, //歌单ID 
        "totalDuration": 0,
        "ordered": false,
        "creator": { //歌单创建者信息
            "birthday": 842871984886, //生日
            "detailDescription": "", //详细描述信息
            "backgroundUrl": "http://p1.music.126.net/peG6dk9pNJlVL8-fURfZvw==/19024849695861456.jpg", //背景图
            "gender": 1,
            "city": 410100, //所在城市
            "signature": "一枚可爱的程序开发爱好汪", //签名
            "description": "", //描述
            "accountStatus": 0,
            "avatarImgId": 109951163688345010,
            "defaultAvatar": false,
            "avatarImgIdStr": "109951163688345003",
            "backgroundImgIdStr": "19024849695861456",
            "province": 410000, //所在省份
            "nickname": "鼻子亲了脸", //昵称
            "djStatus": 0,
            "avatarUrl": "http://p1.music.126.net/qXX85T4PnmIHG2xKIhsbcQ==/109951163688345003.jpg",//头像
            "authStatus": 0, //认证状态
            "vipType": 11, //账号VIP类型 
            "followed": false,
            "userId": 115119971, //用户ID
            "mutual": false,
            "avatarImgId_str": "109951163688345003",
            "authority": 0,
            "userType": 0,
            "backgroundImgId": 19024849695861456
        },
        "subscribers": [],
        "highQuality": false, 
        "commentThreadId": "A_PL_0_2597018357", //歌单评论ID
        "updateTime": 1546580252461, //更新时间
        "trackUpdateTime": 1557322785998, //歌单更新时间
        "userId": 115119971, //歌单创建人ID
        "tracks": [ //音乐信息 此处的音乐信息和上面的音乐详情信息一致,音乐的Json信息太长了,为了简略已经删除
            ........
        ],
        "anonimous": false,
        "tags": [],
        "commentCount": 0, //评论数量
        "cloudTrackCount": 0, //歌单中在网易云盘中音乐的数量
        "coverImgUrl": "https://p1.music.126.net/UN6e5vfw6_c9MRKSEQBVig==/7986852465432828.jpg", //歌单封面
        "playCount": 4, //播放次数
        "coverImgId": 7986852465432828,
        "createTime": 1546580252388,
        "name": "鼻子亲了脸的年度歌单", //歌单名称
        "subscribedCount": 0, //关注数量
        "newImported": false,
        "status": 0 //歌单状态
    }
}

```

## 搜索

说明：搜索关键词可以搜索 音乐 / 歌手 / 专辑 / 歌单 / 视频 / 电台 / 用户 / 歌词

当前支持类型 `song singer album songList video radio user lrc`

接口地址: `netease/search`

请求示例: `netease/search?keyword=花粥&type=song&pageSize=20&page=0`

| 参数说明 | 是否必须 | 说明                                             | 默认值         |
| -------- | -------- | ------------------------------------------------ | -------------- |
| keyword  | ×        | 搜索关键词                                       | 详细见下面说明 |
| type     | ×        | 搜索类型                                         | 默认为 song    |
| pageSize | ×        | 请求数量                                         | 默认为 30      |
| page     | ×        | 分页                                             | 默认第 0 页    |
| format   | X        | 格式化数据(仅格式化音乐搜索) 1 格式化 0 不格式化 | 0              |

## 歌单分类

接口地址: `netease/songList/category`

请求示例: `netease/songList/category`

```json
{
  "code": 200,
  "msg": "OK",
  "timestamp": 1557323584425,
  "data": {
    "all": { //顶级类型 包含所有
      "imgId": 0,
      "activity": false,
      "resourceCount": 1000,
      "name": "全部歌单", //分类名称
      "type": 0,
      "category": 4,
      "hot": false,
      "resourceType": 0
    },
    "sub": [ //子级分类类型
      {
        "imgId": 0,
        "activity": false,
        "resourceCount": 1000,
        "name": "流行",//子级分类名称
        "type": 0,
        "category": 1,
        "hot": true,
        "resourceType": 0
      },
      
      .........

      {
        "imgId": 0,
        "activity": false,
        "resourceCount": 1000,
        "name": "华语",
        "type": 0,
        "category": 0, //父级分类ID
        "hot": true, 
        "resourceType": 0
      }
    ],
    "code": 200,
    "categories": { // 父级分类类型
      "0": "语种", //父级分类ID和名称
      "1": "风格",
      "2": "场景",
      "3": "情感",
      "4": "主题"
    }
  }
}

```

## 精品歌单

接口地址: `netease/songList/highQuality`

请求示例: `netease/songList/highQuality?cat=全部&pageSize=100`

| 参数说明     | 是否必须 | 说明                         | 默认值                               |
| ------------ | -------- | ---------------------------- | ------------------------------------ |
| categoryType | ×        | 歌单分类                     | 默认全部                             |
| orderType    | ×        | 分别对应最新和最热           | 可选值为 'new' 和 'hot',默认为 'hot' |
| pageSize     | ×        | 获取条数                     | 默认 30                              |
| lasttime     | ×        | 上次返回的结果的 lasttime 值 |

## 热门歌单

接口地址: `netease/songList/hot`

请求示例: `netease/songList/hot?cat=全部&pageSize=20&page=0`

| 参数说明     | 是否必须 | 说明               | 默认值                               |
| ------------ | -------- | ------------------ | ------------------------------------ |
| categoryType | ×        | 歌单分类           | 默认全部                             |
| orderType    | ×        | 分别对应最新和最热 | 可选值为 'new' 和 'hot',默认为 'hot' |
| pageSize     | ×        | 获取条数           | 默认 30                              |
| page         | ×        | 分页               | 默认 0                               |

## 用户歌单信息

接口地址:`netease/songList/user`

请求示例: `netease/songList/user?uid=115119971`

| 参数说明 | 是否必须 | 说明    | 默认值  |
| -------- | -------- | ------- | ------- |
| uid      | √        | 用户 ID | 用户 ID |

## MV 信息

接口地址: `netease/mv`

请求示例: `netease/mv?id=10866117`

| 参数说明 | 是否必须 | 说明  | 默认值 |
| -------- | -------- | ----- | ------ |
| id       | √        | MV ID |        |

## MV 播放地址

接口地址: `netease/mvUrl`

请求示例: `netease/mvUrl?id=10866117&quality=1080`

| 参数说明 | 是否必须 | 说明     | 默认值   |
| -------- | -------- | -------- | -------- |
| id       | √        | MVID     |          |
| quality  | ×        | 视频格式 | 默认 480 |

说明: 视频大小类型：1080 720 480 240

## MV 排行榜

接口地址: `netease/mv/top`

请求示例: `netease/mv/top?pageSize=10&page=0`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌手信息

接口地址: `netease/artist/info`

请求示例: `netease/artist/info?id=8103`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 歌手排行榜

接口地址: `netease/artist/top`

请求示例: `netease/artist/top?page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌手歌曲

接口地址: `netease/song/artist`

请求示例: `netease/song/artist?id=8103`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 歌手专辑

接口地址: `netease/album/artist`

请求示例: `netease/album/artist?id=8103`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 歌手 MV

接口地址: `netease/mv/artist`

请求示例: `netease/mv/artist?id=8103`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 最新音乐

接口地址: `netease/song/new`

请求示例: `netease/song/new`

## 最新专辑

接口地址: `netease/album/new`

请求示例: `netease/album/new`

## 音乐评论

接口地址: `netease/comment/song`

请求示例: `netease/comment/song?id=37239038&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌曲 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 专辑评论

接口地址: `netease/comment/album`

请求示例: `netease/comment/album?id=3159845&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 专辑 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## MV 评论

接口地址: `netease/comment/mv`

请求示例: `netease/comment/mv?id=10866117&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | MV ID    |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## Video 评论

接口地址: `netease/comment/video`

请求示例: `netease/comment/video?id=10866117&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | Video ID |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌单评论

接口地址: `netease/comment/songList`

请求示例: `netease/comment/songList?id=2509086690&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌单 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 音乐热门评论

接口地址: `netease/comment/song/hot`

请求示例: `netease/comment/song/hot?id=37239038&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌曲 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 专辑热门评论

接口地址: `netease/comment/album/hot`

请求示例: `netease/comment/album/hot?id=3159845&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 专辑 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## MV 热门评论

接口地址: `netease/comment/mv/hot`

请求示例: `netease/comment/mv/hot?id=10866117&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | MV ID    |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## Video 热门评论

接口地址: `netease/comment/video/hot`

请求示例: `netease/comment/video/hot?id=10866117&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | Video ID |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌单热门评论

接口地址: `netease/comment/songList/hot`

请求示例: `netease/comment/songList/hot?id=2509086690&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌单 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |
