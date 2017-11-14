###### refs

[https://github.com/wyc/semantic-ui-react-todos](https://github.com/wyc/semantic-ui-react-todos)

![image](https://user-images.githubusercontent.com/10850034/32767957-0f1d3f1a-c959-11e7-8950-1f03e06699ab.png)

###### electron化 commit

*   [electronアプリ化](https://github.com/nitaking/electron-react-todolist3/commit/4d02ed981b50e5effc25224d6f5bcd74095231fe)
*   [fix package.json. About 'yarn build'error. · nitaking/electron-react-todolist3@ff9377c](https://github.com/nitaking/electron-react-todolist3/commit/ff9377c01a76fc7d40550826bc15a05fbde7e9fb)

###### [](https://github.com/nitaking/electron-react-todolist3#usage)Usage

[semantic-ui-react-todos](https://github.com/wyc/semantic-ui-react-todos)をelectron化するまでの流れ

1.  .gitを除いてソースファイルだけクローン

```.sh
$ svn export https://github.com/wyc/semantic-ui-react-todos/trunk electron-react-todolist3
```

2.  node_modulesのインストール(今回はyarn使用)

```.sh
$ yarn install
```

3.  electronに必要なライブラリを追加

```.sh
$ yarn add electron     # electron本体
$ yarn add foreman      # 複数プロセス同時起動のため [foreman](https://www.npmjs.com/package/foreman)</code> 
```

4.  ファイルを追加
- src/electron-wait-react.js
- src/electron-starter.js
- Procfile

https://github.com/nitaking/electron-react-todolist3/compare/675714ddefa7e887e436323b3cfc8d50eca93518...4d02ed981b50e5effc25224d6f5bcd74095231fe

5.  package.jsonにforeman用設定を追加

* [package.json](https://github.com/nitaking/electron-react-todolist3/commit/4d02ed981b50e5effc25224d6f5bcd74095231fe#diff-b9cfc7f2cdf78a7f4b91a753d10865a2)

6.  start

```.sh
# Dev
$ yarn dev
```
```.sh
# or build
$ yarn build
$ yarn start</code>
```