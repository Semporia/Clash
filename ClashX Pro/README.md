# 自用整合 ClashX Pro 分流

### ClashX Pro 下载地址

[ClashX Pro Download](https://install.appcenter.ms/users/clashx/apps/clashx-pro/distribution_groups/public)

### 懒人配置参考！

[config.yaml](https://raw.githubusercontent.com/Semporia/Clash/master/ClashX%20Pro/config.yaml)

### 远程引用分流规则

```yaml

# 代理节点
proxy-providers:
  # 所有节点
  机场名:
    type: http
    path: ./Server/机场名.yaml
    url: 订阅连接
    interval: 3600
    filter: '节点关键词'
    health-check:
        enable: true
        url: http://www.gstatic.com/generate_204
        interval: 3600

# 代理组策略
proxy-groups:

# 策略组说明

# 「Proxy」是代理规则策略，它可以指定为某个节点或嵌套一个其他策略组，如：「url-test」（自动测试）、「Fallback」或「load-balance」（负载均衡）的策略组

  - { name: "MATCH", type: select, proxies: ["Proxy"]} 
  - { name: "Apple", type: select, proxies: ["DIRECT"], use: ["United States","Japan"]}
  - { name: "Adobe", type: url-test, use: ["United States"]}
  - { name: "Amazon", type: url-test, use: ["United States"]}
  - { name: "China", type: select, proxies: ["DIRECT"]}
  - { name: "Dler", type: select, use: ["Hong Kong","United States","Dler Cloud"]}
  - { name: "Facebook", type: url-test, use: ["Hong Kong"]}
  - { name: "GitHub", type: url-test, use: ["Hong Kong"]}
  - { name: "Google", type: url-test, use: ["United States"]}
  - { name: "Microsoft", type: select, proxies: ["DIRECT"], use: ["United States"]}
  - { name: "Netflix", type: url-test, use: ["United States"]}
  - { name: "Speedtest", type: select, proxies: ["DIRECT"]} 
  - { name: "Steam", type: url-test, use: ["United States"]}
  - { name: "Spotify", type: url-test, use: ["United States"]}
  - { name: "Telegram", type: url-test, use: ["Hong Kong"]}
  - { name: "Twitter", type: url-test, use: ["Hong Kong"]}
  - { name: "Tencent", type: select, proxies: ["DIRECT"]} 
  - { name: "TencentVideo", type: select, proxies: ["DIRECT"]} 
  - { name: "YouTube", type: url-test, use: ["United States"]}
  - { name: "paypal", type: url-test, use: ["United States"]}
  - { name: "Discord", type: url-test, use: ["United States"]}
  - { name: "Proxy", type: url-test, use: ["Hong Kong","United States"]} 

# 分流规则  
rules:
- RULE-SET,AdBlock,REJECT
- RULE-SET,Proxy,Proxy
- RULE-SET,Apple,Apple
- RULE-SET,Adobe,Adobe
- RULE-SET,Amazon,Amazon
- RULE-SET,Dler,Dler
- RULE-SET,Facebook,Facebook 
- RULE-SET,GitHub,GitHub
- RULE-SET,Google,Google
- RULE-SET,Microsoft,Microsoft
- RULE-SET,Netflix,Netflix 
- RULE-SET,Speedtest,Speedtest
- RULE-SET,Steam,Steam
- RULE-SET,Spotify,Spotify
- RULE-SET,Telegram,Telegram 
- RULE-SET,Twitter,Twitter 
- RULE-SET,Tencent,Tencent
- RULE-SET,TencentVideo,TencentVideo
- RULE-SET,YouTube,YouTube 
- RULE-SET,PayPal,paypal
- RULE-SET,Discord,Discord
- DOMAIN-SUFFIX,live.cn,China

- GEOIP,CN,DIRECT
- MATCH,MATCH

rule-providers:

  AdBlock: {type: http, behavior: classical, path: ./Filter/AdBlock, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/AdBlock.yaml, interval: 3600}
  Apple: {type: http, behavior: classical, path: ./Filter/Apple, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Apple.yaml, interval: 3600}
  Adobe: {type: http, behavior: classical, path: ./Filter/Adobe, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Adobe.yaml, interval: 3600}
  Amazon: {type: http, behavior: classical, path: ./Filter/Amazon, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Amazon.yaml, interval: 3600}

  China: {type: http, behavior: classical, path: ./Filter/China, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/China.yaml, interval: 3600}

  Dler: {type: http, behavior: classical, path: ./Filter/Dler, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Dler.yaml, interval: 3600}

  Facebook: {type: http, behavior: classical, path: ./Filter/Facebook, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Facebook.yaml, interval: 3600}

  GitHub: {type: http, behavior: classical, path: ./Filter/GitHub, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/GitHub.yaml, interval: 3600}
  Google: {type: http, behavior: classical, path: ./Filter/Google, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Google.yaml, interval: 3600}
  
  Microsoft: {type: http, behavior: classical, path: ./Filter/Microsoft, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Microsoft.yaml, interval: 3600}
  
  Netflix: {type: http, behavior: classical, path: ./Filter/Netflix, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Netflix.yaml, interval: 3600}
  
  Spotify: {type: http, behavior: classical, path: ./Filter/Spotify, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Spotify.yaml, interval: 3600}
  Speedtest: {type: http, behavior: classical, path: ./Filter/Speedtest, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Speedtest.yaml, interval: 3600}
  Steam: {type: http, behavior: classical, path: ./Filter/Steam, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Steam.yaml, interval: 3600}

  Telegram: {type: http, behavior: classical, path: ./Filter/Telegram, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Telegram.yaml, interval: 3600}
  Twitter: {type: http, behavior: classical, path: ./Filter/Twitter, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Twitter.yaml, interval: 3600}
  Tencent: {type: http, behavior: classical, path: ./Filter/Tencent, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Tencent.yaml, interval: 3600}
  TencentVideo: {type: http, behavior: classical, path: ./Filter/TencentVideo, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/TencentVideo.yaml, interval: 3600}

  YouTube: {type: http, behavior: classical, path: ./Filter/YouTube, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/YouTube.yaml, interval: 3600}

  PayPal: {type: http, behavior: classical, path: ./Filter/PayPal, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/PayPal.yaml, interval: 3600}
  Discord: {type: http, behavior: classical, path: ./Filter/Discord, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Discord.yaml, interval: 3600}
  Proxy: {type: http, behavior: classical, path: ./Filter/Proxy, url: https://raw.githubusercontent.com/Semporia/Clash/master/Rule/Proxy.yaml, interval: 3600}

```
