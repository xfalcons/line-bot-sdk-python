# Flask Echo

Sample echo-bot using [Flask](http://flask.pocoo.org/)

## Getting started

```
$ export LINE_CHANNEL_SECRET=YOUR_LINE_CHANNEL_SECRET
$ export LINE_CHANNEL_ACCESS_TOKEN=YOUR_LINE_CHANNEL_ACCESS_TOKEN

$ pip install -r requirements.txt
```

Run WebhookParser sample

```
$ python app.py
```

Run WebhookHandler sample

```
$ python app_with_handler.py
```

# line-bot-python-heroku
***
API : [https://devdocs.line.me/en/](https://devdocs.line.me/en/)  
line-bot-sdk-python : [https://github.com/line/line-bot-sdk-python](https://github.com/line/line-bot-sdk-python)  
Fixie : [https://elements.heroku.com/addons/fixie](https://elements.heroku.com/addons/fixie)
***

1. 註冊Line Messaging API  
[https://business.line.me/zh-hant/services/bot](https://business.line.me/zh-hant/services/bot)  
 - 記下`Channel Access Token``Channel Secret`

2. Deploy 到 Heroku (需先註冊Heroku帳號)  
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/xfalcons/line-bot-sdk-python/tree/to-heroku/examples/flask-echo)

3. 修改app.py參數  
`line_bot_api = LineBotApi('') #Your Channel Access Token`  
`handler = WebhookHandler('') #Your Channel Secret` 

4. Add-ons Fixie  
[https://elements.heroku.com/addons/fixie](https://elements.heroku.com/addons/fixie) 

5. 到Line developers 設定`Webhook URL`  
`https://{YOUR_HEROKU_SERVER_ID}.herokuapp.com/callback`