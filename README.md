wrangler.jsonc：
 
 "name": "xxx", // 替换为你的cloudflare page的名字

 "proxy_url": "https://your-proxy-domain.com", // 替换为你的代理服务器域名, 必须为https
 
 "token_prefix": "/default/" // 替换为你想设置的访问密码。首尾斜杠必须保留，如果密码为空，表示不需要密码也可以访问。

Docker部署：
1 配置 SSL 证书和 Nginx：配置域名对应的 SSL 证书和 Nginx，将其指向本地的 5006 端口

2 克隆仓库：执行命令：git clone https://github.com/netptop/siteproxy.git

3 编辑配置文件：打开并修改 config.json 文件，内容如下：
{
   "proxy_url": "https://your-proxy-domain.com", // 替换为你申请到的代理服务器域名
   "token_prefix": "/user-SetYourPasswordHere/",  // 设置网站密码，用于防止非法访问，保留首尾的斜杠
   "description": "注意：token_prefix 相当于网站密码，请谨慎设置。 proxy_url 和 token_prefix 合起来就是访问网址。"
}

4 启动 Docker 容器：进入 docker-node 子目录。执行命令：sudo docker compose up

5 访问代理服务：现在可以通过 https://your-proxy-domain.com/user-your-password/ 访问代理服务。请将域名和密码替换为你自己的域名和密码。
