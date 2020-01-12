# trojan
### 不加密便是最好的加密
trojan做为一款新的FQ工具，一般的科学上网采用强加密和随机混淆来欺骗GFW的过滤机制。然而，Trojan采用最常见的协议HTTPS，在设计时采用了更适应国情的思路，以诱骗GFW认为它是HTTPS。当Trojan客户端连接到服务器时，它首先执行真正的 TLS握手。如果握手成功，则所有后续流量都将受到保护TLS; 否则，服务器将立即关闭连接，就像任何HTTPS服务器一样。Trojan反侦查采用主动检测与被动检测，主动检测：没有正确结构和密码的所有连接将被重定向到预设端点，因此HTTP如果可疑探针连接（或者只是您连接到博客XD的粉丝），则特洛伊木马服务器的行为与该端点完全相同（默认情况下）。被动检测：由于流量受到保护TLS（用户有责任使用有效证书），如果您正在访问某个HTTP站点，则流量看起来与HTTPS（握手RTT后只有一个TLS）相同; 如果您没有访问某个HTTP站点，那么流量看起来就像HTTPS保持活动一样WebSocket。因此，木马也可以绕过ISP QoS限制。

### tojan类似于v2ray的 ws+tls 都是模仿常见的web服务，但较v2ray ws+tls更轻便化，亲测比 ws+tls快

[阿里云APIKey地址](https://usercenter.console.aliyun.com)      [CloudFlare APIkey地址](https://dash.cloudflare.com/efeb3f1f4b0940ed5c2bf595c05903b4/profile/api-tokens)      [vultr APIkey地址](https://my.vultr.com/settings/#settingsapi)

# 一键脚本

![image](https://github.com/voiin/trojan/blob/master/trojan.png)
## CentOS
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/voiin/trojan/master/install_trojan.sh && bash install_trojan.sh
```
## Debian or Ubuntu
```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/voiin/trojan/master/install_trojan_de.sh && bash install_trojan_de.sh
```
