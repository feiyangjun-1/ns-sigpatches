### 简体中文（当前页面/U R HERE）| [ENGLISH (TRANSLATING)](\README_EN.md)
# 自行构建 sigpatches 教程 （制作中。。。）
1. 下载最新版[IPS Patch Creator](https://github.com/mrdude2478/IPS_Patch_Creator/releases/latest)
2. 下载[`Lockpick_RCM.bin`](https://codeberg.org/attachments/466940a5-9bcb-42db-a0de-1038b2a132ad)（此为备份，[原仓库](https://github.com/shchmue/Lockpick_RCM)因版权原因已被 Github 删除）
3. 下载你当前使用的系统固件，可以在[此处](https://darthsternie.net/switch-firmwares/)或[此处](https://github.com/THZoria/NX_Firmware/releases)进行下载
4. 以 RCM 模式启动，注入 `Lockpick_RCM.bin`，按音量键选择你需要 dump 的系统（有虚拟系统就选 Dump from EmuNAND，反之则选择 Dump from SysNAND），按电源键确认
5. 稍等片刻，按电源键退出，选择 Reboot <RCM>
6. 将储存卡取出，使用电脑读取。在根目录下的 `switch` 文件夹中使用记事本（或其他软件）打开 `prod.keys` 文件
7. 解压下载好的 IPS Patch Creator，在解压好的文件夹中创建名为 `Firmware` 的文件夹，将下载好的系统固件中的所有文件解压到 `Firmware` 文件夹中
8. 打开 IPS Patch Creator 文件夹中的 `tools` 文件夹，将 `prod.keys` 中的数据对照填入
9. 打开 `IPS_Patch_Creator.exe` 
