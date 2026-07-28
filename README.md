# FFXIV 台服 Dalamud API 13 插件庫

這是給 FFXIV 台灣版 Dalamud API 13 使用的自訂插件來源。

## 自訂來源網址

```text
https://raw.githubusercontent.com/yuanhs2186/FFXIV-TW-Plugins/main/pluginmaster.json
```

將以上網址加入 Dalamud 設定的自訂插件來源，儲存後重新整理插件清單。

## 收錄插件

| 插件 | 版本 | API | 說明 |
| --- | --- | --- | --- |
| Artisan 繁體中文台服版 | 4.0.4.61 | 13 | 基於 MeowZWR 4.0.4.6-cn 製作並轉為繁體中文 |
| AutoDuty 繁體中文台服版 | 0.0.278.1 | 13 | 基於 erdelf/AutoDuty 0.0.0.278 重新編譯並繁體中文化 |
| AutoRetainer | 4.5.4.12 | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| Yes Already | 1.13.5 | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| AntiAfkKick | 2.1.0.9 | 13 | 防止角色因閒置而被自動踢出 |
| TextAdvance | 3.2.4.7 | 13 | 自動略過對話並確認跳過過場動畫 |
| vnavmesh 中文版 | 0.2.8.0 | 13 | AutoDuty 必要尋路插件；AtmoOmen 官方歷史 Release |
| Avarice | 2.1.1.6 | 13 | 從最後一版 API13 原始碼重新編譯 |
| Lifestream | 2.5.3.5 | 13 | AutoDuty 建議的傳送與移動配套 |
| Pandora's Box | 1.6.3.22 | 13 | AutoDuty 建議的實用自動化配套 |
| Stylist | 1.0.0.11 | 13 | AutoDuty 建議的裝備推薦配套 |
| Gearsetter | 4.0 | 13 | AutoDuty 裝備推薦 IPC；官方歷史 API13 Release |
| BossMod Reborn | 7.3.8.41 | 13 | AutoDuty 必要戰鬥與機制插件；略過台服不存在的 InventoryAck Hook |
| GatherBuddy Reborn | 7.3.0.24 | 13 | 修正自動換裝後以舊職業執行採集技能造成的 Invalid job selected |
| Rotation Solver Reborn | 7.3.0.71 | 13 | 台服實機驗證；重編譯主插件與內建技能組，修正 DTR API 不相容 |
| Sonar | 0.7.4.1 | 13 | 狩獵與特殊 FATE 情報接收、轉發 |
| Item Vendor Location | 2.11.0.0 | 13 | 從物品選單查詢商人位置 |
| EnemyListDebuffs | 1.13.0.0 | 13 | 在敵人列表顯示自身施加的減益 |
| Target Lines | 1.9.0.0 | 13 | goatcorp 官方 API13 歷史套件 |
| XIV Combo Expanded | 2.0.4.1 | 13 | 連擊合併單鍵；以 API14 更新前最後一版原始碼重新編譯 |

## 注意事項

- 不要同時啟用兩個 `InternalName` 相同的 Artisan。
- Artisan 保留原本的 `InternalName: Artisan`，因此會沿用既有設定檔。
- AutoDuty 仍需要 BossMod Reborn、vnavmesh 與支援的戰鬥循環插件。
- Gearsetter 使用 VeraNala 保存的官方 v4.0 API13 Release；Stylist 仍可作為另一個裝備推薦來源。
- 第三方插件可能違反遊戲服務條款，請自行評估並承擔使用風險。

## Artisan 檔案雜湊

`Artisan-TW-4.0.4.61.zip`

SHA-256：

```text
43CB9A39154EFF37FCD8B1424CFD754C6F3CF3B6D70A15C899030E7DCD2D7864
```
