# Shanbay-Alfred2-Workflow

[![CircleCI](https://circleci.com/gh/alswl/shanbay-alfred2.svg?style=svg)](https://circleci.com/gh/alswl/shanbay-alfred2)

扇贝网 Alfred2 workflow，主要用于单词查询、添加单词到词库、发音。


## 安装

下载 [`Shanbay.alfredworkflow`](https://github.com/alswl/shanbay-alfred2/releases) 里面的最新版本。

双击文件导入即可。


## 使用

-   授权
    -   任意使用查询功能，如 `sb love` 会检查权限情况，如果权限不存在或过期，会自动进入授权页面
    -   在扇贝官网的授权界面输入帐号密码，然后授权
    -   出现 `Shanbay OAuth2` 之后，将完整的 URL 复制下来，并在 Alfred 里面输入
        `sbauth https://www.shanbay.com/oauth2/auth/success/#access_token=SAMPLE&token_type=Bearer&state=&expires_in=2592000&scope=read+write`
        （后面的 URL 请替换为你自己复制的 URL）
        -   注意：在 2019-10 月之后，这个页面打开会是 404 页面，但是不影响使用
    -   授权完成，使用 `sb love` 测试，按回车即可以添加到单词库
-   查单词
    -   使用 `sb love` 查询单词
-   添加到单词库
    -   使用 `sb love` 查询单词，然后使用回车即添加到单词库
-   打开单词
    -   使用 `sb love` 查询单词，按住 `Command` + 回车，打开扇贝官网对应的单词页面
-   听发音
    -   使用 `sb love` 查询单词，按住 `Ctrl` + 回车，即可播放语音


注：授权有效期为一个月，过期需重新授权。


## 截图

-   ![love](https://github.com/alswl/shanbay-alfred2/raw/master/snapshot/sb_love.png)
-   ![auth](https://github.com/alswl/shanbay-alfred2/raw/master/snapshot/sb_auth.png)
-   ![sound](https://github.com/alswl/shanbay-alfred2/raw/master/snapshot/sb_sound.png)


## 其它

感谢原作者 [henter/Shanbay-Alfred2](https://github.com/henter/Shanbay-Alfred2)  开发初始版本。

我的改进：

-   不使用 code 授权模式，改为 token 直接授权，不用打开一个第三方网站（也是因为原来那个授权网站挂掉，我才改造的）
-   支持发音
-   移除例句查询功能
-   移除 `requests` 依赖，即装即用
-   支持新版本检查


## 打包

```
make
```
