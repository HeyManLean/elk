## 创建网络

```
docker network create --subnet=192.168.0.1/16
```

### Elatsticsearch

- 额外安装 `elasticsearch-head`
```
vi config/elasticsearch.yml
# 添加
http.cors.enabled: true
http.cors.allow-origin: "*"

vi /etc/resolv.conf
# 修改 nameserver 为 8.8.8.8 删除其他行

yum update
yum install -y vim unzip git wget

# 安装 node
curl --silent --location https://rpm.nodesource.com/setup_10.x | bash
yum -y install nodejs
npm install -g cnpm --registry=https://registry.npm.taobao.org

# 安装 head
wget https://github.com/mobz/elasticsearch-head/archive/master.zip
unzip master.zip
cd elasticsearch-head-master
npm install
cnpm install
npm run start
```