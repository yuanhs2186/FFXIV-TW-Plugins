# FFXIV 台服 Dalamud API 13 插件庫

這是給 FFXIV 台灣版 Dalamud API 13 使用的自訂插件來源，主要收錄 AutoDuty 與相關配套，以及經過台服相容性修正的插件。

最後核對日期：**2026-07-29**

## 安裝方式

在 Dalamud 的「設定 → 測試版 → 自訂插件庫」新增：

```text
https://raw.githubusercontent.com/yuanhs2186/FFXIV-TW-Plugins/main/pluginmaster.json
```

儲存並啟用來源後，回到插件安裝器重新整理清單。

若剛更新 GitHub 後仍顯示舊版本，通常是 GitHub Raw 或 Dalamud 快取尚未刷新。請等待幾分鐘後重新整理；Dalamud API 或 runtime 剛更新時，完整重開遊戲最可靠。

## 版本編號說明

插件版本不等於 FFXIV 遊戲版本。

例如：

- `BossMod Reborn 7.3.8.4` 是 BossMod Reborn 的插件版本，不代表遊戲版本「7.38」。
- 本庫的 `7.3.8.41` 表示以 `7.3.8.4` 為基底製作的台服相容修正版。
- GatherBuddy、Rotation Solver、vnavmesh 等插件各自採用不同版本規則，不能只用數字大小互相比較。

國際服上游目前已進入較新的 API 與遊戲資料版本，直接使用最新版本不一定能在台服 API 13 載入。本庫以「台服實際能載入及使用」為優先，不以追上國際服最高版本號為目標。

台服介面雖可能顯示遊戲開放版本為 7.2，但實際客戶端包含部分 7.3 技能與資料。因此相容性以 Dalamud API、實際客戶端、載入日誌及遊戲測試為準。

## 重要相容性選擇

部分其他 API 13 來源雖顯示較大的 `7.3.8.x` 版本，但仍保留台服會出錯的程式碼，所以本庫沒有直接換用。

| 插件 | 本庫版本 | 採用原因 |
| --- | --- | --- |
| BossMod Reborn | `7.3.8.41` | 基於上游 `7.3.8.4`；台服找不到 `InventoryAck` signature 時改為停用該項 hook，而不是讓整個插件載入失敗 |
| GatherBuddy Reborn | `7.3.0.24` | 處理台服 `ClientLanguage`、尚未存在的魚類／藏寶圖資料，以及換職後 `Invalid job selected` |
| Rotation Solver Reborn | `7.3.0.71` | 針對台服 Dalamud API 13 重編譯並帶入技能組，避開不相容的 DTR API |
| vnavmesh | `0.2.8.0` | 採用已確認可配合 AutoDuty 的 AtmoOmen 中文 API 13 版本；不同來源的版本號不可直接比較 |

已檢查到的其他 API 13 套件：

- BossMod Reborn `7.3.8.3` 仍強制建立台服不存在的 `InventoryAck` hook，會重現載入失敗。
- GatherBuddy Reborn `7.3.8.14` 仍會把台服語言值傳入只支援 EN／DE／FR／JP 的名稱表，會重現 `ArgumentException`。
- Rotation Solver Reborn `7.3.8.27` 仍呼叫台服 API 13 缺少的 DTR `OnClick`，會反覆出現 `Method not found`。

因此「數字較大」不代表在目前台服環境較新或較穩定。

## 收錄插件

| 插件 | 版本 | API | 說明 |
| --- | --- | --- | --- |
| Artisan 繁體中文台服版 | `4.0.4.61` | 13 | 基於 MeowZWR `4.0.4.6-cn` 製作並轉為繁體中文 |
| AutoDuty 繁體中文台服版 | `0.0.278.2` | 13 | 基於 erdelf/AutoDuty `0.0.0.278` 重新編譯並繁體中文化 |
| AutoRetainer | `4.5.4.12` | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| Yes Already | `1.13.5` | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| AntiAfkKick | `2.1.0.9` | 13 | 防止角色因閒置而被自動踢出 |
| TextAdvance | `3.2.4.7` | 13 | 自動略過對話並確認跳過過場動畫 |
| vnavmesh 中文版 | `0.2.8.0` | 13 | AutoDuty 必要尋路插件；AtmoOmen 中文 API 13 Release |
| Avarice | `2.1.1.6` | 13 | 從 API 13 原始碼重新編譯 |
| Lifestream | `2.5.3.5` | 13 | AutoDuty 建議的傳送與移動配套 |
| Pandora's Box | `1.6.3.22` | 13 | AutoDuty 建議的實用自動化配套 |
| Stylist | `1.0.0.11` | 13 | AutoDuty 建議的裝備推薦配套 |
| Gearsetter | `4.0` | 13 | AutoDuty 裝備推薦 IPC；官方歷史 API 13 Release |
| BossMod Reborn | `7.3.8.41` | 13 | AutoDuty 戰鬥與機制插件；含台服 `InventoryAck` 相容修正 |
| GatherBuddy Reborn | `7.3.0.24` | 13 | 台服語言、資料與自動換職相容修正 |
| Rotation Solver Reborn | `7.3.0.71` | 13 | 台服 API 13 主插件與技能組 |
| Sonar | `0.7.4.1` | 13 | 狩獵與特殊 FATE 情報接收、轉發 |
| Item Vendor Location | `2.11.0.0` | 13 | 從物品選單查詢商人位置 |
| EnemyListDebuffs | `1.13.0.0` | 13 | 在敵人列表顯示自身施加的減益 |
| Target Lines | `1.9.0.0` | 13 | goatcorp API 13 歷史套件 |
| XIV Combo Expanded | `2.0.4.1` | 13 | 連擊合併單鍵；以 API 14 更新前最後一版原始碼重新編譯 |
| AutoHook | `5.0.0.11` | 13 | 釣魚自動提鉤；以 API 14 更新前最後一版原始碼重新編譯 |
| Wrath Combo | `1.0.2.17` | 13 | 連擊合併進化版；Yuki 保存的官方 API 13 Release，與 XIV Combo 擇一使用 |

實際安裝版本以 [`pluginmaster.json`](./pluginmaster.json) 為準；README 與來源版本不同時請提出回報。

## AutoDuty 基本配套

AutoDuty 至少需要：

- BossMod Reborn
- vnavmesh
- 一個支援的戰鬥循環插件，例如 Rotation Solver Reborn

依使用功能不同，也可能需要 AutoRetainer、Yes Already、Lifestream、Pandora's Box、Avarice、Stylist、Gearsetter、GatherBuddy Reborn 或 AutoHook。

不要同時啟用兩個 `InternalName` 相同的插件。解除安裝插件通常不會刪除 `pluginConfigs` 內的使用者設定，但更新前仍建議先備份。

## 其他台服 API 13 來源

CycleApple 的來源主要提供 Penumbra、Glamourer、Customize+、Brio、Simple Tweaks 等外觀與便利插件，與本庫內容互補，可另外新增：

```text
https://raw.githubusercontent.com/cycleapple/DalamudPlugins-TW/main/repo.json
```

不建議把相同插件從多個來源同時安裝；若不同來源具有相同 `InternalName`，只保留已確認可用的一個來源版本。

## 注意事項

- 第三方插件可能違反遊戲服務條款，請自行評估並承擔使用風險。
- 台服更新遊戲、Dalamud 或 API 後，插件可能需要重新編譯或修正 signature。
- 顯示 API 13 只代表 manifest 宣告相符，不保證遊戲資料、Dalamud 方法與 signature 一定相容。

## Artisan 檔案雜湊

`Artisan-TW-4.0.4.61.zip`

SHA-256：

```text
43CB9A39154EFF37FCD8B1424CFD754C6F3CF3B6D70A15C899030E7DCD2D7864
```
