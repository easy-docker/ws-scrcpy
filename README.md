# ws scrcpy 的 Docker 镜像

用来在浏览器中控制 Android 设备。

https://hub.docker.com/r/ghostry/ws-scrcpy
https://github.com/easy-docker/ws-scrcpy/

## 使用

```
docker run --name ws-scrcpy -d -p 8000:8000 ghostry/ws-scrcpy
docker exec ws-scrcpy adb connect android.device.ip:5555
```

注意修改 android.device.ip 为 Android 设备 IP 地址。

## 打开 Android 设备的 adb over Wi-Fi

1. 安装 adb 工具套件（[SDK Platform Tools](https://developer.android.com/studio/releases/platform-tools)）
2. 打开开发者模式
3. 使用 USB 连接 Android 设备，并授权
4. 终端输入 `adb tcpip 5555`

返回 `restarting in TCP mode port: 5555` 即可.  
切换回USB模式：`adb usb`

## 参考链接

* https://github.com/scavin/ws-scrcpy-docker/
