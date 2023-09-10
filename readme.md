# go-midjourney

golang语言实现, 代理 MidJourney 的discord频道，实现api形式调用AI绘图


## 支持功能
- [x] 支持 Imagine 指令和相关U、V操作
- [x] Imagine 时支持添加图片base64，作为垫图
- [x] 支持 Describe 指令，根据图片生成 prompt
- [x] 支持 Blend 指令，多个图片混合
- [ ] 支持 Imagine、V、Blend 图片生成进度
- [ ] 支持 ZoomOut 扩图
- [ ] 支持 Shorten 指令
- [ ] 支持中文 prompt 翻译，需配置百度翻译或 gpt
- [ ] prompt 敏感词判断，支持覆盖调整
- [ ] 任务队列，默认队列10，并发3。可参考 [MidJourney订阅级别](https://docs.midjourney.com/docs/plans) 调整DISCORD_QUEUE_SIZE
- [ ] user-token 连接 wss，可以获取错误信息和完整功能
- [ ] 支持 discord域名(server、cdn、wss)反代，配置 mj.ng-discord
- [ ] 暴露 swagger API文档
- [ ] 支持多个频道，配置 DISCORD_CHANNEL_IDS
- [ ] 同事支持回调模式和进度查询模式

## 使用前提
1. 注册 MidJourney，创建自己的频道，参考 https://docs.midjourney.com/docs/quick-start
2. 获取用户Token、服务器ID、频道ID：

## 风险须知
1. 建议使用bot模式，避免账号封禁


## 配置项
```nashorn yaml
# discord 配置
DISCORD_USER_TOKEN: 你的用户token
DISCORD_BOT_TOKEN: 你的机器人token
DISCORD_SERVER_ID: 你的discord服务器id
DISCORD_CHANNEL_ID: 你的discord频道id
CB_URL: 获取到discord中的图片资源传输给你的业务服务接口
MJ_PORT: 16007
```



