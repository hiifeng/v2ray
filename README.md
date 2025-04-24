# v2ray
V2ray多合一脚本，支持VMESS+websocket+TLS+Nginx、VLESS+TCP+XTLS、VLESS+TCP+TLS等组合

脚本原作者为网络跳越，网络跳越由于工作原因，停止维护该脚本，目前由ifeng开始维护。维护后的脚本可以在纯ipv6网络环境的主机上使用。使用过程中遇到问题，欢迎进入Tg群组（ https://t.me/HiaiFeng ）交流。

脚本支持：
<li>VMESS，即最普通的V2ray服务器，没有伪装，也不是VLESS</li>
<li>VMESS+KCP，传输协议使用mKCP，VPS线路不好时可能有奇效</li>
<li>VMESS+TCP+TLS，带伪装的V2ray，不能过CDN中转</li>
<li>VMESS+WS+TLS，即最通用的V2ray伪装方式，能过CDN中转，推荐使用</li>
<li>VLESS+KCP，传输协议使用mKCP</li>
<li>VLESS+TCP+TLS，通用的VLESS版本，不能过CDN中转，但比VMESS+TCP+TLS方式性能更好</li>
<li>VLESS+WS+TLS，基于websocket的V2ray伪装VLESS版本，能过CDN中转，有过CDN情况下推荐使用</li>
<li>VLESS+TCP+XTLS，目前最强悍的VLESS+XTLS组合，强力推荐使用（但是支持的客户端少一些）</li>
<li>TROJAN</li>
<li>TROJAN+XTLS(推荐)</li>
<br>
<p>安装方法：</p>
bash <(curl -sL https://raw.githubusercontent.com/hiifeng/v2ray/main/install_v2ray.sh)<br>
如果没有出现安装菜单，CentOS系统请输入 yum install -y curl，Ubuntu/Debian系统请输入 sudo apt install -y curl，然后再次运行上面的命令。<br>
<br>
<p>维护更新：</p>
2023年12月23日<br>
<p>修改脚本判断域名是否解析正确的Bug。</p>
2022年12月14日<br>
<p>修改在ipv4&ipv6双栈主机下，DNS同时解析ipv4和ipv6记录，脚本判断域名是否解析正确的Bug。</p>
2022年12月09日<br>
<p>升级TLS版本，排除安全隐患，提高nginx性能。</p>
2022年11月29日<br>
<p>解决通过Github API获取v2ray最新版本失败问题，Github API对于普通用户限制（x-ratelimit-limit）每小时只允许60次请求。对于ipv6 only主机在使用dns64后，由于出口ipv4地址一致，当多人同时调用Github API，造成超出限额，获取v2ray最新版本失败。</p>
2022年11月03日<br>
<p>修改访问伪装网站提示error code: 1034错误。</p>
2022年10月24日<br>
<p>修改VLESS启动失败bug。</p>
2022年10月18日<br>
1、修改纯ipv6网络环境下，申请ssl证书失败等bug。<br>
2、修改安装V2ray最新版本v5.1.0程序异常bug。

<br>赞助声明：<br>
本项目由 [VTEXS](https://console.vtexs.com/?affid=1539) 的「开源项目免费 VPS 计划」提供算力支持。<br>
感谢 VTEXS 对开源社区的支持！<br>
