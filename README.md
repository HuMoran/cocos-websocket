# cocos-websocket
A small decorator for the cocos-creator WebSocket API that automatically reconnects.
# eg:
```js
const ReWebSocket = require('./websocket');
ws = new ReWebSocket('ws://xxxx');
ws.onopen = () => {
  console.log('websocket open');
  ws.send('hello server');
};
ws.opclose = () => {
  console.log('websocket closed');
};
ws.onmessage = (event) => {
  console.log('received msg', event.data);
};
```