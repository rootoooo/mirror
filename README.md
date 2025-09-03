wrangler.jsonc：
 
 "name": "xxx", // 替换为你的cloudflare page的名字

 "proxy_url": "https://your-proxy-domain.com", // 替换为你的代理服务器域名, 必须为https
 
 "token_prefix": "/default/" // 替换为你想设置的访问密码。首尾斜杠必须保留，如果密码为空，表示不需要密码也可以访问。

进入clone的siteproxy目录，执行:npm run wrangler-login, 如果是非GUI的VPS环境，请参考非GUI环境wrangler login

执行:npm run deploy-cf-page
