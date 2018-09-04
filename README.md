用于计算 IM、LiveRoom、RTCRoom 以及 WebRTC 等方案中所需要使用的 **UserSig** 和 **privateMapKey** 签名，算法基于 ECDSA-SHA256 实现

有**php**、**java**和**nodejs**版本

## privateMap 与 privateMapKey

| 权限说明| 对应的privateMap(16进制)| 对应的privateMap(10进制)| 
| ------| ------| ------|
| 推流+观看| 0xff | 255 |
| 观看| 0xab | 171 |

十进制的值将作为明文的权限位在参数中直接调用。
如果业务侧考虑安全问题，就对这个权限位进行加密，用密文的方式传输，源码。

计算**privateMapKey**的时候有个参数**dwPrivilegeMap**表示权限位，代码中默认都是0xff，即拥有全部权限，您可以根据需要调整**dwPrivilegeMap**
