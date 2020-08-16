### Chromecast receiver emulator for google sdk v2

***Note:  This doesn't work, please don't get your hopes up :(***

## Features:

1. python tornado websocket service as chromecast Host
2. transfer messages between receiver (web app) and sender (mobile)

## example
```
    from ChromecastEmulator import MessageHandler
    application = tornado.web.Application([
        (r'/v2/ipc', MessageHandler),
        (r'/sender', MessageHandler)
    ])
    application.listen(8008)
    tornado.ioloop.IOLoop.instance().start()
```

## Todo:
1. implement wifi broadcasting to be visible for mobile app
2. only tested for hulu, and need to test for other web app, e.g. youtube, netflix

