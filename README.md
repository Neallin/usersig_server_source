用于计算 IM、LiveRoom、RTCRoom 以及 WebRTC 等方案中所需要使用的 **UserSig** 和 **privateMapKey** 签名，算法基于 ECDSA-SHA256 实现

有**php**、**java**和**nodejs**版本

### 什么是 UserSig 
https://cloud.tencent.com/document/product/647/17275

### 什么是 privateMapKey
https://cloud.tencent.com/document/product/647/17275#privatemap-.E4.B8.8E-privatemapkey

计算**privateMapKey**的时候有个参数**dwPrivilegeMap**表示权限位，代码中默认都是0xff，即拥有全部权限，如果您可以根据需要调整**dwPrivilegeMap**

对照表如下：

| 权限说明| 对应的privateMap(16进制)| 对应的privateMap(10进制)| 
| ------| ------| ------|
| 推流+观看| 0xff | 255 |
| 观看| 0xab | 171 |
