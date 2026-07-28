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
| AutoDuty | 0.0.0.278 | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| AutoRetainer | 4.5.4.12 | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| Yes Already | 1.13.5 | 13 | 使用 YukiDalamudPlugins 的台服相容套件 |
| AntiAfkKick | 2.1.0.9 | 13 | 防止角色因閒置而被自動踢出 |
| TextAdvance | 3.2.4.7 | 13 | 自動略過對話並確認跳過過場動畫 |
| vnavmesh 中文版 | 0.2.8.0 | 13 | AutoDuty 必要尋路插件；AtmoOmen 官方歷史 Release |
| Avarice | 2.1.1.6 | 13 | 從最後一版 API13 原始碼重新編譯 |
| Lifestream | 2.5.3.5 | 13 | AutoDuty 建議的傳送與移動配套 |
| Pandora's Box | 1.6.3.22 | 13 | AutoDuty 建議的實用自動化配套 |
| Stylist | 1.0.0.11 | 13 | AutoDuty 建議的裝備推薦配套 |
| Boss Mod | 7.3.0.108 | 13 | AutoDuty 必要戰鬥與機制插件；適配 2026.07.22 台服客戶端 |
| GatherBuddy Reborn | 7.3.0.23 | 13 | 台服實機驗證；修正繁中語言初始化並略過未開放的 7.3 採集資料 |
| Rotation Solver Reborn | 7.3.0.7 | 13 | AutoDuty 可用的戰鬥循環插件 |
| Sonar | 0.7.4.1 | 13 | 狩獵與特殊 FATE 情報接收、轉發 |
| Item Vendor Location | 2.11.0.0 | 13 | 從物品選單查詢商人位置 |
| EnemyListDebuffs | 1.13.0.0 | 13 | 在敵人列表顯示自身施加的減益 |
| Target Lines | 1.9.0.0 | 13 | goatcorp 官方 API13 歷史套件 |

## 注意事項

- 不要同時啟用兩個 `InternalName` 相同的 Artisan。
- Artisan 保留原本的 `InternalName: Artisan`，因此會沿用既有設定檔。
- AutoDuty 仍需要 BossMod、vnavmesh 與支援的戰鬥循環插件。
- Gearsetter 的原始 Git 主機已失效，目前找不到可驗證的 API13 套件，因此暫不收錄；Stylist 可先提供同類裝備推薦功能。
- 第三方插件可能違反遊戲服務條款，請自行評估並承擔使用風險。

## Artisan 檔案雜湊

`Artisan-TW-4.0.4.61.zip`

SHA-256：

```text
43CB9A39154EFF37FCD8B1424CFD754C6F3CF3B6D70A15C899030E7DCD2D7864
```
