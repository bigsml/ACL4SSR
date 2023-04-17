# ChatGPT 使用

因为ChatGPT 不支持香港节点，所以需要建立GPT 的独立规则 
参考[https://github.com/wgetnz/chatgpt-openclash]
基于 ACL4SSR 的 WithChinaIp_WithGFW 基础规则构建

1. 转化订阅 
https://api.dler.io/sub?target=clash&new_name=true&url=你的订阅链接(需要使用URL编码)&config=https%3A%2F%2Fraw.githubusercontent.com%2Fbigsml%2FACL4SSR%2Fmaster%2FClash%2Fconfig%2FACL4SSR_WithChinaIp_WithGFW_chatGPT.ini

2. clash 订阅以上规则即可 

# 注意事项

chatgpt 的网站启用了 http3 ，基于 quic ，基于 udp 如果出现还不能指定节点的情况，请开启UDP 代理，就算开启了 UDP 代理，因为 V2RAY 不支持 http3 的域名嗅探，所以基于域名的路由规则就失效了。不要全局，要不就只能基于 geoip 来。
最简单的是把浏览器的 http3 支持给关了：（重要）
chrome://flags/#enable-quic
edge://flags/#enable-quic
降级成 http1/2 就能让域名路由规则生效了。
