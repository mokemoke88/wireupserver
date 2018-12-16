# @seekers/wireupserver

net::Serverオブジェクトに,残っている接続を強制切断してclose()するメソッドを追加するパッチ関数

## functions

createWireup(server: Server): WireupServer;

## usage

``` typescript
import * as http from 'http';
import { createWireup } from '@seekers/wireupserver';

const server = createWireup(http.createServer(...));

// anything do it.

server.destroy(()=>{
  console.log('server closed.');
});
```

## 参考URL

- [node + express で Graceful Shutdown 実装でハマったので共有](https://qiita.com/waterada/items/baafa41c262712defc34)
