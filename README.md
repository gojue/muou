# muou(木偶)
muou是一个网络包测试工具，可以自定义TCP Option的内容，用于测试4层网络设备的处理情况。


## 用法
修改Maximum segment size，MSS值为：`1460`。
* Kind: Maximum Segment Size (2)
* Length: 4
* MSS Value: 1460

字节内容即为`020405b4`，其中`02`表示Kind，`04`表示Length，`05b4`表示MSS Value。


```shell
sudo ./muou t -b 020405b4
```

# 关于开源
暂不开源，部分厂商的L4LB 四层负载均衡设备的缺陷还未完全升级。以后再说。

# 参考
* [eCapture旁观者](https://github.com/gojue/ecapture)
* [TCP segment structure](https://en.wikipedia.org/wiki/Transmission_Control_Protocol#TCP_segment_structure)
* [Transmission Control Protocol (TCP) Parameters](https://www.iana.org/assignments/tcp-parameters/tcp-parameters.xhtml)
