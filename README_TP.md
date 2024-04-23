### [簡體中文](/README.md) | [正體字（中華台北，當前頁面）] | [英語](/README_EN.md)
### 注：由於作者是大陸人，不清楚台灣當地用詞習慣，但也已盡量轉換爲台灣用詞。不當之處可以透過 pull requests 提交修改申請！
##### 如果你是懶人，可以直接在 [Release](https://github.com/feiyangjun-1/ns-sigpatches/releases/latest) 中下載已經製作好的 sigpatches。
#### 注意：按照此教程最後生成的 sigpatches 只適用於你選擇的系統韌體版本以及大氣層版本，不向上或向下兼容。
# 準備工作
* 最新版 [IPS Patch Creator](https://disk.yandex.com/d/LEKGKbfDw-_pjA)
* [`Lockpick_RCM.bin`](https://codeberg.org/attachments/466940a5-9bcb-42db-a0de-1038b2a132ad)（此為備份，[原倉庫](https://github.com/shchmue/Lockpick_RCM)因版權原因已被 Github 刪除）。
* 下載你當前使用的設備系統韌體。可以在 [Darthsternie's Firmware Archive](https://darthsternie.net/switch-firmwares/) 或 [THZoria/NX_Firmware](https://github.com/THZoria/NX_Firmware/releases) 進行下載。
* 下載你需要使用的[大氣層](https://github.com/Atmosphere-NX/Atmosphere/releases)版本。
# 第一步 - 提取密鑰
1. 以 RCM 模式啟動你的設備，注入 `Lockpick_RCM.bin`
2. 按音量鍵進行選擇。如果你使用的是虛擬系統，請選擇 Dump from EmuNAND；反之則選擇 Dump from SysNAND。按電源鍵確認。
3. 稍等片刻，待導出完成後，按電源鍵退出，選擇 Shutdown （也可按照情況選擇其他選項）。
4. 將 SD 卡取出，使用電腦讀取。在 SD 卡根目錄底下的 `/switch/` 資料夾中使用記事本（或其他軟件）打開 `prod.keys` 檔案。
5. 解壓下載好的 IPS Patch Creator。在解壓好的資料夾中創建名為 Firmware 的資料夾，將下載好的系統韌體壓縮包中的所有檔案解壓到 `/Firmware/` 資料夾中。
6. 打開 IPS Patch Creator 資料夾中的 `/tools/` 資料夾，將 `prod.keys` 中的數據對照填入至 `keys.dat` 檔案中。
# 第二步 - 生成簽名補丁（sigpatches）
1. 在 IPS Patch Creator 資料夾中解壓下載好的大氣層壓縮包。
2. 打開 `IPS_Patch_Creator.exe` 。在 IPS Creator 下的 Loader 選項卡中，點選文字框下方的 Make Patch 按鈕。在彈出的對話框中點選解壓的大氣層中 `/atmosphere/` 資料夾中的 `package3` 檔案，點擊打開。
3. 切換至 ES 選項卡，點選 Make Patch 按鈕。在彈出的對話框中點選 IPS Patch Creator 資料夾中的 `/Firmware/` 資料夾，點擊確定。
4. 切換至 ES2 選項卡，點選 Make Patch 按鈕。在彈出的對話框中點選 IPS Patch Creator 資料夾中的 `/Firmware/` 資料夾，點擊確定。
5. 切換至 FS 選項卡，點選 Make Patch 按鈕。在彈出的對話框中點選 IPS Patch Creator 資料夾中的 `/Firmware/` 資料夾，點擊確定。
6. 切換至 NFIM 選項卡，點選 Make Patch 按鈕。在彈出的對話框中點選 IPS Patch Creator 資料夾中的 `/Firmware/` 資料夾，點擊確定。
# 第三步 - 完成
1. 將 IPS Patch Creator 資料夾中的 `atmosphere` 和 `bootloader` 兩個資料夾複製到 SD 卡根目錄底下。
   * 若提示有相同檔案，選擇覆蓋即可。
2. 開玩！

最後，有問題歡迎在 issues 中提問！
