# 🌌 太空人葆葆肚子餓了

這是一款以「無重力太空場域」為背景的互動式 VR 體驗。玩家將化身為太空人「葆葆」，在漂浮環境中抓取食物並投入儲存箱，完成任務以免於飢餓「漂浮餓死」。

---

## 📦 專案資訊

- **開發平台**：Unity 2022.3.x (LTS, Silicon)
- **開發設備**：MacBook M1
- **測試方式**：XR Device Simulator（無實體 Meta Quest 測試設備）
- **目標平台**：Meta Quest (Android)
- **最終建置**：Windows 桌機 .exe 可執行檔

---

## 🛠 開發流程

### 1. macOS 製作與模擬
- 在 Unity 中選擇 `Android` 為 Build Platform（Meta Quest 相容）
- 使用 **XR Device Simulator** 進行互動測試（滑鼠鍵盤操作模擬抓取）
- 實作抓取食物、投放、過關邏輯等流程

### 2. 專案移轉至 Windows 打包
- 將整個專案資料夾（含 `Assets`、`Packages`、`ProjectSettings` 等）複製至 Windows
- 使用 Unity Hub 開啟專案並 `Switch Platform → Windows`
- 透過 `Build & Run` 建置為 `.exe` 執行檔

---

## 💡 開發建議（跨平台開發策略）

本專案採用跨平台開發策略，兼顧模擬與展示需求：

### 🧪 macOS 開發與模擬階段
- Build Platform 設為 **Android**，對應 Meta Quest
- 使用 XR Device Simulator 模擬 VR 操作（滑鼠與鍵盤）
- 無需實體裝置，即可完成大多數互動與流程測試

### 📦 Windows 打包為非 VR 展示版本
- 切換平台為 **Windows**
- 輸出 `.exe` 可執行檔，方便進行非 VR 展示（例如報告、展場互動等）

此策略大幅提升開發效率，並保有展示彈性。

---

## ⚠ 注意事項

- 使用 **URP** 或 **3D Core**，請勿使用 HDRP
- 插件建議使用 `Meta XR All-in-One SDK`（具跨平台相容性）
- 所有資源請存放於 `Assets/` 資料夾內，避免使用硬編碼路徑
- 建議開發與打包皆使用 Unity 2022.3.x LTS 版本（Meta 官方推薦）

---

## 📝 建立紀錄
- 記錄建立時間：2025-05-30
