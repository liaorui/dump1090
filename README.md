dump接口里增加radar标识，标记每台设备的渠道号。

```
// Structure used to describe an aircraft in iteractive mode
struct aircraft {
    ......
    char          radar[20];         // marking this device
    ......
};

```

原理是，读取每台设备的/etc/hostname值，赋给radar变量。

在多台设备部署时，需要配置好每台设备的/etc/hostname，进行区分。
