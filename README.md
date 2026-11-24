# HZFOTA

Air780EPM OneNET 纯脚本 FOTA 升级包托管仓库。

## 文件

| 文件 | 大小 | 说明 |
|---|---|---|
| `ONENET_HZ_1.0.1.bin` | 8661 B | LuatOS 纯脚本升级包（magic `18 72 C3 EA`），项目 ONENET_HZ，版本 1.0.1（连接后先报 FOTA_STATUS 再报 VERSION，与 1.0.0 相反） |

包内**不含**设备密钥（DEVICE_KEY）。密钥在烧录基线固件时写入设备 fskv，升级脚本从 fskv 读取。

## 用法

OneNET 物模型下发：

- `FOTA_URL` = 本仓库文件的 raw 直链
- `FOTA` = 1（正常升级）或 2（强制重刷）

直链格式：

```
https://raw.githubusercontent.com/Qzkqqq/HZFOTA/main/ONENET_HZ_1.0.1.bin
```

注意：raw 直链要求仓库为 **Public**，设备端无法携带 GitHub 凭据下载私有仓库。
