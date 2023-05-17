### 简体中文（当前页面/U R HERE）| [正體中文（中華台北）](/README_TP.md) | [ENGLISH](/README_EN.md)
##### 如果你是懒人，可以直接在 [Release](https://github.com/feiyangjun-1/ns-sigpatches/releases/latest) 中下载已经制作好的 sigpatches。
#### 注意：按照此教程最后生成的 sigpatches 只适用于你选择的的系统固件版本以及大气层版本，不向上或向下兼容。
# 你都得准备点啥？
* 最新版 [IPS Patch Creator](https://github.com/mrdude2478/IPS_Patch_Creator/releases/latest)
* [`Lockpick_RCM.bin`](https://codeberg.org/attachments/466940a5-9bcb-42db-a0de-1038b2a132ad)（此为备份，[原仓库](https://github.com/shchmue/Lockpick_RCM)因版权原因已被 Github 删除）。
* 下载你当前使用的设备系统固件。可以在 [Darthsternie's Firmware Archive](https://darthsternie.net/switch-firmwares/) 或 [THZoria/NX_Firmware](https://github.com/THZoria/NX_Firmware/releases) 进行下载。
* 下载你需要使用的[大气层](https://github.com/Atmosphere-NX/Atmosphere/releases)版本。
# 第一步 - 提取密钥
1. 以 RCM 模式启动你的设备，注入 `Lockpick_RCM.bin`
2. 按音量键进行选择。如果你使用的是虚拟系统，请选择 Dump from EmuNAND；反之则选择 Dump from SysNAND。按电源键确认。
3. 稍等片刻，待导出完成后，按电源键退出，选择 Shutdown （也可按照情况选择其他选项）。
4. 将 SD 卡取出，使用电脑读取。在 SD 卡根目录下的 `/switch/` 文件夹中使用记事本（或其他软件）打开 `prod.keys` 文件。
5. 解压下载好的 IPS Patch Creator。在解压好的文件夹中创建名为 `/Firmware/` 的文件夹，将下载好的系统固件压缩包中的所有文件解压到 `/Firmware/` 文件夹中。
6. 打开 IPS Patch Creator 文件夹中的 `/tools/` 文件夹，将 `prod.keys` 中的数据对照填入至 `keys.dat` 文件中。
# 第二步 - 生成签名补丁（sigpatches）
1. 在 IPS Patch Creator 文件夹中解压下载好的大气层压缩包。
2. 打开 `IPS_Patch_Creator.exe` 。在 IPS Creator 下的 Loader 选项卡中，点击文字框下方的 Make Patch 按钮。在弹出的对话框中选择解压的大气层中 `/atmosphere/` 文件夹中的 `package3` 文件，点击打开。
3. 切换至 ES 选项卡，点击 Make Patch 按钮。在弹出的对话框中选择 IPS Patch Creator 文件夹中的 `/Firmware/` 文件夹，点击确定。
4. 切换至 ES2 选项卡，点击 Make Patch 按钮。在弹出的对话框中选择 IPS Patch Creator 文件夹中的 `/Firmware/` 文件夹，点击确定。
5. 切换至 FS 选项卡，点击 Make Patch 按钮。在弹出的对话框中选择 IPS Patch Creator 文件夹中的 `/Firmware/` 文件夹，点击确定。
6. 切换至 NFIM 选项卡，点击 Make Patch 按钮。在弹出的对话框中选择 IPS Patch Creator 文件夹中的 `/Firmware/` 文件夹，点击确定。
# 第三步 - 完成
1. 将 IPS Patch Creator 文件夹中的 `atmosphere` 和 `bootloader` 两个文件夹复制到 SD 卡根目录。
   * 若提示有相同文件，选择覆盖即可。
2. 开玩！

最后，有问题欢迎在 issues 中提问！如果你觉得有些地方的语言有些晦涩，可以通过 pull requests 申请修改！
