# QQ 音乐

## 获取音乐详情

接口地址: `https://v1.itooi.cn/tencent/song`

请求示例: `https://v1.itooi.cn/tencent/song?id=003OUlho2HcRHC,001fXNWa3t8EQQ`

| 参数说明 | 是否必须 | 说明                                                | 默认值 |
| -------- | -------- | --------------------------------------------------- | ------ |
| id       | √        | 音乐 ID,可一次获取多首音乐信息,必须使用英文逗号分开 | 无     |
| format   | x        | 格式化数据 1 格式化 0 不格式化                      | 0      |

## 获取音乐播放地址

接口地址: `https://v1.itooi.cn/tencent/url`

请求示例: `https://v1.itooi.cn/tencent/url?id=003OUlho2HcRHC,001fXNWa3t8EQQ&quality=flac`

| 参数说明   | 是否必须 | 说明                                      | 默认值                     |
| ---------- | -------- | ----------------------------------------- | -------------------------- |
| id         | √        | 音乐 ID                                   | 无                         |
| quality    | √        | 音质 如果最大音质获取出错则自动转其他音质 | 默认 192                   |
| isRedirect | ×        | 是否 302 跳转                             | 1 跳转 0 不跳转 默认为跳转 |

说明: 码率类型：48 96 128 192 320 ape flac

## 获取音乐歌词

接口地址: `https://v1.itooi.cn/tencent/lrc`

请求示例: `https://v1.itooi.cn/tencent/lrc?id=003OUlho2HcRHC`

| 参数说明 | 是否必须 | 说明    | 默认值           |
| -------- | -------- | ------- | ---------------- |
| id       | √        | 音乐 ID | 默认获取翻译歌词 |

## 获取音乐图片

接口地址: `https://v1.itooi.cn/tencent/pic`

请求示例: `https://v1.itooi.cn/tencent/pic?id=003OUlho2HcRHC`

| 参数说明   | 是否必须 | 说明          | 默认值                                       |
| ---------- | -------- | ------------- | -------------------------------------------- |
| id         | √        | 音乐 ID       |                                              |
| imgSize    | √        | 音乐 ID       | 默认获取 200x200 大小的图片 其他大小自行尝试 |
| isRedirect | ×        | 是否 302 跳转 | 1 跳转 0 不跳转 默认为跳转                   |

## 获取专辑详情

接口地址: `https://v1.itooi.cn/tencent/album`

请求示例: `https://v1.itooi.cn/tencent/album?id=003RMaRI1iFoYd`

| 参数说明 | 是否必须 | 说明                           | 默认值 |
| -------- | -------- | ------------------------------ | ------ |
| id       | √        | 专辑 ID                        | 无     |
| format   | x        | 格式化数据 1 格式化 0 不格式化 | 0      |

## 音乐歌单

说明：获取歌单中的所有音乐

接口地址: `https://v1.itooi.cn/tencent/songList`

请求示例: `https://v1.itooi.cn/tencent/songList?id=7073731347`

| 参数说明 | 是否必须 | 说明                           | 默认值 |
| -------- | -------- | ------------------------------ | ------ |
| id       | √        | 歌单的 ID                      | 无     |
| format   | x        | 格式化数据 1 格式化 0 不格式化 | 0      |

## 搜索

说明：搜索关键词可以搜索 音乐 / 歌手 / 专辑 / 歌单 / 视频 / 电台 / 用户 / 歌词

当前支持类型 `song singer album songList video radio user lrc`

接口地址: `https://v1.itooi.cn/tencent/search`

请求示例: `https://v1.itooi.cn/tencent/search?keyword=喜欢你&type=song&pageSize=100&page=0`

| 参数说明 | 是否必须 | 说明                                             | 默认值         |
| -------- | -------- | ------------------------------------------------ | -------------- |
| keyword  | √        | 搜索关键词                                       | 详细见下面说明 |
| type     | √        | 搜索类型                                         | 默认为 song    |
| pageSize | ×        | 请求数量                                         | 默认为 30      |
| page     | ×        | 分页                                             | 默认第 0 页    |
| format   | x        | 格式化数据(仅格式化音乐搜索) 1 格式化 0 不格式化 | 0              |

## 排行榜

接口地址: `https://v1.itooi.cn/tencent/topList`

请求示例: `https://v1.itooi.cn/tencent/topList?id=26&pageSize=100&page=0&format=1`

| 参数说明 | 是否必须 | 说明                           | 默认值  |
| -------- | -------- | ------------------------------ | ------- |
| id       | √        | 排行榜 ID                      |         |
| format   | x        | 格式化数据 1 格式化 0 不格式化 | 0       |
| pageSize | ×        | 获取条数                       | 默认 30 |
| page     | ×        | 分页                           | 默认 0  |

## 歌单分类

接口地址: `https://v1.itooi.cn/tencent/songList/category`

请求示例: `https://v1.itooi.cn/tencent/songList/category`

## 热门歌单

接口地址: `https://v1.itooi.cn/tencent/songList/hot`

请求示例: `https://v1.itooi.cn/tencent/songList/hot?categoryId=10000000&sortId=5&pageSize=10&page=1`

| 参数说明   | 是否必须 | 说明     | 默认值                             |
| ---------- | -------- | -------- | ---------------------------------- |
| categoryId | ×        | 分类 ID  | ID 见歌单分类接口返回数据          |
| sortId     | ×        | 排序 ID  | ID 见歌单分类接口返回数据          |
| pageSize   | ×        | 获取条数 | 默认 30 官方限制分页条数最大 60 条 |
| page       | ×        | 分页     | 默认 0                             |

## 用户歌单信息

接口地址:`tencent/songList/user`

请求示例: `https://v1.itooi.cn/tencent/songList/user?uid=32432434`

| 参数说明 | 是否必须 | 说明    | 默认值  |
| -------- | -------- | ------- | ------- |
| uid      | √        | 用户 ID | 用户 ID |

## 获取 MV 信息

接口地址: `https://v1.itooi.cn/tencent/mv`

请求示例: `https://v1.itooi.cn/tencent/mv?id=m00238resnh`

| 参数说明 | 是否必须 | 说明  | 默认值 |
| -------- | -------- | ----- | ------ |
| id       | √        | MV ID |        |

## 获取 MV 播放地址

接口地址: `https://v1.itooi.cn/tencent/mvUrl`

请求示例: `https://v1.itooi.cn/tencent/mvUrl?id=m00238resnh&quality=1080`

| 参数说明   | 是否必须 | 说明          | 默认值                     |
| ---------- | -------- | ------------- | -------------------------- |
| id         | √        | MVID          |                            |
| quality    | ×        | 视频格式      | 默认 480                   |
| isRedirect | ×        | 是否 302 跳转 | 1 跳转 0 不跳转 默认为跳转 |

说明: 视频大小类型：1080 720 480 240

## 歌单分类

接口地址: `https://v1.itooi.cn/tencent/mv/category`

请求示例: `https://v1.itooi.cn/tencent/mv/category`

## 热门 MV

接口地址: `https://v1.itooi.cn/tencent/mv/hot`

请求示例: `https://v1.itooi.cn/tencent/mv/hot?&pageSize=100&page=0`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌手详情

接口地址: `https://v1.itooi.cn/tencent/artist`

请求示例: `https://v1.itooi.cn/tencent/artist?id=003kBi0c1ckZB4`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 歌手分类

接口地址: `https://v1.itooi.cn/tencent/artist/category`

请求示例: `https://v1.itooi.cn/tencent/artist/category`

## 歌手列表

接口地址: `https://v1.itooi.cn/tencent/artist/list`

请求示例: `https://v1.itooi.cn/tencent/artist/list?sexId=-100&areaId=-100&genre=-100&index=-100&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值    |
| -------- | -------- | -------- | --------- |
| sexId    | ×        | 性别 ID  | -100 全部 |
| areaId   | ×        | 地区 ID  | -100 全部 |
| genre    | ×        | 类型 ID  | -100 全部 |
| index    | ×        | 索引     | -100 全部 |
| pageSize | ×        | 获取条数 | 默认 30   |
| page     | ×        | 分页     | 默认 0    |

## 歌手音乐

接口地址: `https://v1.itooi.cn/tencent/song/artist`

请求示例: `https://v1.itooi.cn/tencent/song/artist?id=003kBi0c1ckZB4`

| 参数说明 | 是否必须 | 说明                           | 默认值  |
| -------- | -------- | ------------------------------ | ------- |
| id       | ×        | 歌手 ID                        |         |
| pageSize | ×        | 获取条数                       | 默认 30 |
| page     | ×        | 分页                           | 默认 0  |
| format   | x        | 格式化数据 1 格式化 0 不格式化 | 0       |

## 歌手专辑

接口地址: `https://v1.itooi.cn/tencent/album/artist`

请求示例: `https://v1.itooi.cn/tencent/album/artist?id=003kBi0c1ckZB4`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 歌手 MV

接口地址: `https://v1.itooi.cn/tencent/mv/artist`

请求示例: `https://v1.itooi.cn/tencent/mv/artist?id=003kBi0c1ckZB4`

| 参数说明 | 是否必须 | 说明    | 默认值 |
| -------- | -------- | ------- | ------ |
| id       | ×        | 歌手 ID |        |

## 首页轮播图

接口地址: `https://v1.itooi.cn/tencent/banner`

请求示例: `https://v1.itooi.cn/tencent/banner`

## 音乐评论

接口地址: `https://v1.itooi.cn/tencent/comment/song`

请求示例: `https://v1.itooi.cn/tencent/comment/song?id=003OUlho2HcRHC&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌曲 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 专辑评论

接口地址: `https://v1.itooi.cn/tencent/comment/album`

请求示例: `https://v1.itooi.cn/tencent/comment/album?id=003RMaRI1iFoYd&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 专辑 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## MV 评论

接口地址: `https://v1.itooi.cn/tencent/comment/mv`

请求示例: `https://v1.itooi.cn/tencent/comment/mv?id=m00238resnh&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | MV ID    |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 榜单评论

接口地址: `https://v1.itooi.cn/tencent/comment/top`

请求示例: `https://v1.itooi.cn/tencent/comment/top?id=26&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 榜单 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌单评论

接口地址: `https://v1.itooi.cn/tencent/comment/songList`

请求示例: `https://v1.itooi.cn/tencent/comment/songList?id=7073731347&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌单 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 音乐热门评论

接口地址: `https://v1.itooi.cn/tencent/comment/song/hot`

请求示例: `https://v1.itooi.cn/tencent/comment/song/hot?id=003OUlho2HcRHC&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌曲 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 专辑热门评论

接口地址: `https://v1.itooi.cn/tencent/comment/album/hot`

请求示例: `https://v1.itooi.cn/tencent/comment/album/hot?id=003RMaRI1iFoYd&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 专辑 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## MV 热门评论

接口地址: `https://v1.itooi.cn/tencent/comment/mv/hot`

请求示例: `https://v1.itooi.cn/tencent/comment/mv/hot?id=m00238resnh&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | MV ID    |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 榜单热门评论

接口地址: `https://v1.itooi.cn/tencent/comment/top/hot`

请求示例: `https://v1.itooi.cn/tencent/comment/top/hot?id=26&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 榜单 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |

## 歌单热门评论

接口地址: `https://v1.itooi.cn/tencent/comment/songList/hot`

请求示例: `https://v1.itooi.cn/tencent/comment/songList/hot?id=7073731347&page=0&pageSize=30`

| 参数说明 | 是否必须 | 说明     | 默认值  |
| -------- | -------- | -------- | ------- |
| id       | ×        | 歌单 ID  |         |
| pageSize | ×        | 获取条数 | 默认 30 |
| page     | ×        | 分页     | 默认 0  |
