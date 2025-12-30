首先申请Bot API Token

向官方 @BotFather 申请一个机器人，获得 Bot API Token，

发送/setjoingroups来禁止此Bot被他人添加到群组，发送/setjoingroups后选择你的 bot，再发送 Disable即可。

创建 Worker

配置worker的变量

增加一个ENV_BOT_TOKEN变量，值为向官方 bot申请的Bot API Token

增加一个ENV_BOT_SECRET变量，SECRET值为uuid

增加一个ENV_ADMIN_UID变量，值为用户id

创建一个命名空间KV数据库 随意名字

绑定KV数据库，变量名称：telegrambot,KV命名空间：选择设置的数据库名字

编辑代码 将worker代码全部复制替换原来的代码，保存部署（注意先设置好变量，KV数据库之后在部署代码，不然有可能报错代码部署不了）

url后面加上/registerWebhook，进行 webhook注册 (unRegisterWebhoo 取消注册) 出现OK表示成功！

测试时先点开自己机器人点一下开始，就能正常接收消息了
