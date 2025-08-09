`
# Telegram-BOT搭建
`
## 创建机器人，申请Token
```bash
@BotFather
```
## 创建群组
把机器人设置为管理员，群设置为公开，然后改为私有，并允许话题模式
通过@GetTheirIDBot获取个人ID和群组ID

## 安装Docker
```bash
bash <(curl -sL 'https://get.docker.com')
```
## 安装1Panel
```bash
bash -c "$(curl -sSL https://resource.fit2cloud.com/1panel/package/v2/quick_start.sh)"
```
## 安装虚拟环境
```bash
apt install python3-venv supervisor
```
## 部署代码
```bash
cd /srv
git clone https://github.com/MiHaKun/Telegram-interactive-bot.git
cd Telegram-interactive-bot
python3 -m venv venv
. venv/bin/activate
pip install -r requirements.txt
```
## 进入1Panel
点击主机——文件——顶部搜索
```bash
/srv/Telegram-interactive-bot
```
## 获取API_ID，API_HASH
```bash
https://my.telegram.org
```
## 打开 .env_example 文件
```
修改Bot-Token，ADMIN_GROUP_ID,ADMIN_USER_IDS
之后再下方添加   API_ID=     API_HASH=
保存——退出——文件命名为.env
```
## 工具箱
进程守护——初始化（按操作重启）——创建守护进程

## 名称  (启动用户不变)
```bash
tgbot-InteractiveBot
```
## 运行目录
```bash
/srv/Telegram-interactive-bot
```
## 启动命令
```bash
/srv/Telegram-interactive-bot/venv/bin/python -m interactive-bot
```
## 保存


