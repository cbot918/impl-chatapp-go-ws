1. websocket 原理

   1.1. http upgrade request

   1.2. socket connection with 6455 format

   1.3. ping/pong 機制

   1.4. readystate 意思

2. websocket library 實作

   2.1. upgrader

   2.2. codec frame

   2.3. handle ping/pong

   2.4. read/write json

3. golang websocket 的選擇

   3.1. Fork 3.5K / Star 20.3k: [gorilla/websocket](https://github.com/gorilla/websocket)

   3.2. Fork 866 / Star 5.4k: [go-socketio](https://github.com/googollee/go-socket.io)

   3.4. Fork 13 / Star 104: [socket.io](https://github.com/zishang520/socket.io)

   3.3. Fork 386 / Star 3.4k:[melody](https://github.com/olahol/melody)

4. 開始做聊天室

   4.1. 核心功能: chat / room / history_message / users / 已讀 / @

   4.2. 技術選擇: gorilla / gin / mysql

   4.2. gorilla 跟 gin 的互動

   4.3. database schema

   4.4. pkg/caht, pkg/client, store

   4.5. handlers

   4.6. web ui 的部份

   4.7. demo

   4.8. 壓測 / profile

5. 優化及架構擴展方向

   5.1. profile 工具

   5.2. 現有程式碼的改善 (著重減少 goroutine / buffer 的使用)

   5.3. 往底層改善: 打開 maxfd / 使用非同步 epoll / 使用優化過的 gobwas-ws / 打開 XX 表

   5.4. 往架構改善: logic-queue-comet 架構 / gateway-serverless 架構

6. 還可以做些什麼？

   6.1. 聊天室實作上線: 可以練習把 code 寫好寫乾淨

   6.2. 試著 go-socketio 支援 最新版: 講一下 go-socketio 跟 engine-io 的關係

   6.3. 自己練習刻 protocol [autobahn-testsuite](https://github.com/crossbario/autobahn-testsuite): 可以增加通訊協定及網路底層的知識

   6.4. 練習實作 epoll / gopool [gobwas/ws](https://github.com/gobwas/ws): 可以增加作業系統方面的知識

   6.5. 練習服務拆分 [bilibili/goim](https://github.com/Terry-Mao/goim): 增加架構設計知識
