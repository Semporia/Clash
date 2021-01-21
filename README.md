# 自用整合ClashX 分流

### ClashX 下载地址

[ClashX Download](https://install.appcenter.ms/users/clashx/apps/clashx-pro/distribution_groups/public)

### 懒人配置参考！

[config.yaml](https://raw.githubusercontent.com/Semporia/ClashX-Pro/master/config.yaml)

### 远程引用分流规则

```properties

rule-providers:

  AdBlock:
    type: http
    behavior: classical
    path: ./Filter/AdBlock.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/AdBlock.yaml
    interval: 86400
  
  DIRECT:
    type: http
    behavior: classical
    path: ./Filter/DIRECT.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/DIRECT.yaml
    interval: 86400

  Domestic:
    type: http
    behavior: classical
    path: ./Filter/Domestic.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Domestic.yaml
    interval: 86400

  Microsoft:
    type: http
    behavior: classical
    path: ./Filter/Microsoft.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Microsoft.yaml
    interval: 86400

  Netease Music:
    type: http
    behavior: classical
    path: ./Filter/Netease Music.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Netease Music.yaml
    interval: 86400

  Adobe:
    type: http
    behavior: classical
    path: ./Filter/Adobe.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Adobe.yaml
    interval: 86400

  GitHub:
    type: http
    behavior: classical
    path: ./Filter/GitHub.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/GitHub.yaml
    interval: 86400

  Apple:
    type: http
    behavior: classical
    path: ./Filter/Apple.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Apple.yaml
    interval: 86400

  PayPal:
    type: http
    behavior: classical
    path: ./Filter/PayPal.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/PayPal.yaml
    interval: 86400

  Google:
    type: http
    behavior: classical
    path: ./Filter/Google.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Google.yaml
    interval: 86400

  YouTube:
    type: http
    behavior: classical
    path: ./Filter/YouTube.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/YouTube.yaml
    interval: 86400

  Telegram:
    type: http
    behavior: classical
    path: ./Filter/Telegram.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Telegram.yaml
    interval: 86400

  Twitter:
    type: http
    behavior: classical
    path: ./Filter/Twitter.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Twitter.yaml
    interval: 86400

  Facebook:
    type: http
    behavior: classical
    path: ./Filter/Facebook.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Facebook.yaml
    interval: 86400

  Amazon:
    type: http
    behavior: classical
    path: ./Filter/Amazon.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Amazon.yaml
    interval: 86400

  Spotify:
    type: http
    behavior: classical
    path: ./Filter/Spotify.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Spotify.yaml
    interval: 86400

  Speedtest:
    type: http
    behavior: classical
    path: ./Filter/Speedtest.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Speedtest.yaml
    interval: 86400

  Steam:
    type: http
    behavior: classical
    path: ./Filter/Steam.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Steam.yaml
    interval: 86400

  AsianTV:
    type: http
    behavior: classical
    path: ./Filter/AsianTV.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/AsianTV.yaml
    interval: 86400

  Netflix:
    type: http
    behavior: classical
    path: ./Filter/Netflix.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Netflix.yaml
    interval: 86400

  Proxy:
    type: http
    behavior: classical
    path: ./Filter/Proxy.yaml
    url: https://raw.githubusercontent.com/Semporia/Clash-X/master/Filter/Proxy.yaml
    interval: 86400

# 分流规则  
rules:
  
  # (AdBlock)
  - RULE-SET,AdBlock,AdBlock 

  # (DIRECT)
  - RULE-SET,DIRECT,DIRECT 

  # (Domestic)
  - RULE-SET,Domestic,Domestic

  # (Microsoft)
  - RULE-SET,Microsoft,Microsoft

  # (Netease Music)
  - RULE-SET,Netease Music,DIRECT

  # (Adobe)
  - RULE-SET,Adobe,Adobe

  # (GitHub)
  - RULE-SET,GitHub,GitHub

  # (Apple)
  - RULE-SET,Apple,Apple

  # (PayPal)
  - RULE-SET,PayPal,paypal 

  # (Google)
  - RULE-SET,Google,Google

  # (YouTube)
  - RULE-SET,YouTube,YouTube 
  
  # (Telegram)
  - RULE-SET,Telegram,Telegram 
  
  # (Twitter)
  - RULE-SET,Twitter,Twitter 
  
  # (Facebook)
  - RULE-SET,Facebook,Facebook 
  
  # (Amazon)
  - RULE-SET,Amazon,Amazon 
  
  # (Spotify)
  - RULE-SET,Spotify,Proxy 
  
  # (Speedtest)
  - RULE-SET,Speedtest,DIRECT

  # (Steam)
  - RULE-SET,Steam,Proxy

  # (AsianTV)
  - RULE-SET,AsianTV,AsianTV

  # (Netflix)
  - RULE-SET,Netflix,Netflix

  # (Proxy)
  - RULE-SET,Proxy,Proxy

  # GeoIP China
  - GEOIP,CN,DIRECT
  - MATCH,MATCH

```