
server 端部署需要先创建一个数据库 `thewho`：
```shell
$ mysql -u root -p

// create database thewho;
```
然后装一下依赖：
```shell
$ cd coco-server & npm i
```
接着修改一下我们的数据库配置，可以根据本地 `mysql` 配置来调整：
```js
module.exports = {
  sequelize: {
    dialect: 'mysql',
    host: '127.0.0.1',
    port: 3306,
    database: 'thewho',
    username: 'root',
    password: 'root1234',
    logging: false
  }
};
```
最后:
```shell
$ npm run dev
```
会自动创建 `project`、`template` 数据表。正常启动后，可以看到我们的服务启动 `http://localhost:70001`。

