# WebRTC  

[谷歌官网](https://webrtc.org/?hl=zh-cn)  
[AppRTC GitHub](https://github.com/webrtc/apprtc)  
[Unity WebRTC Tutorial](https://docs.unity3d.com/Packages/com.unity.webrtc@3.0/manual/tutorial.html)  
[知乎参考一](https://zhuanlan.zhihu.com/p/525416889)  
[知乎参考二](https://zhuanlan.zhihu.com/p/525424241)  
[参考文档](https://developer.mozilla.org/zh-CN/docs/Web/API/WebRTC_API)  
[参考视频一](https://www.bilibili.com/video/BV1D14y1W7qp/?spm_id_from=333.337.search-card.all.click&vd_source=e41e557c965196efc71b2d5de8ad6f36)  
[参考视频二](https://www.bilibili.com/video/BV1NG4y1s77c/?spm_id_from=333.337.search-card.all.click&vd_source=e41e557c965196efc71b2d5de8ad6f36)

## 协议
1. **媒体协商**  
SDP(Session Description Protocol)：Peer双方需要交换SDP信息，双方才可互相了解，也称为 **“媒体协商”**。 e.g. 视频通信的双方互相知道可支持的视频解码方式。
2. **网络协商**  
(1)获取外网IP地址映射；（2）通过信令服务器（signal server）交换"网络信息"  
**NAT（Network Address Translation，网络地址转换）** 将局域网IP映射到公网IP+端口  
**STUN（Session Traversal Utilities for NAT，NAT会话穿越应用程序）** 允许位于NAT后的客户端找出自己的公网地址，判断路由器阻止直连的限制方法协议  
**TURN（Traversal Using Relays around NAT）** 某些情况无法点对点连接，就需要使用公网中继服务器转发，转发协议定义为TURN，一对一单向数据200kbps，双方接受共200kbps*4数据  

**ICE（Interactive Connectivity Establishment）** IEC采用了SDP、NAT、STUN、TURN完成端对端传输
## 信令服务器
- SDP、Candidate的交换  
- 房间管理及其人员进出  
## 一对一通信图解
![通信原理](/通信原理.png)
This sentence uses `$` delimiters to show math inline:  $\sqrt{3x-1}+(1+x)^2$  $$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$

