# npm_storage_build
npm仓库搭建



# verdaccio搭建npm私有仓库
## 安装node
## 安装verdaccio  npm i -g verdaccio --unsafe-perm
## 安装pm2 npm i -g pm2 --unsafe-perm
## 配置
    * verdaccio 启动
    * /root/.config/verdaccio/config.yaml 在配置文件结束加 listen: 0.0.0.0:4873
    * 配置文件修改后 verdaccio -c config.yml
    * 配置文件里镜像地址可改为阿里的  https://registry.npm.taobao.org/
    * 修改阿里云策略组放开4873端口
    * pm2 start verdaccio pm2 save
    * 查看是否搭建完成 http://yourip:4873/
    * 登上verdaccio建立账户
## 客户端发包到服务器
    * 将npm地址换成 服务器地址
    * npm login / npm adduser   --registry  http://yourip:4873
    * npm version patch major minor...(具体可查询)
    * npm publish --registry  http://yourip:4873
 

## 配置参数 
    * https://verdaccio.org/docs/en/installation.html
