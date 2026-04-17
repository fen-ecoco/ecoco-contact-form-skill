---
name: ecoco-advanced-customer-form
description: 協助建立與維護高質感的 ECOCO 客服表單 (Customer Service Form)，具備工單號碼自動產生、會員資料自動帶入、階層式可搜尋下拉選單、支援預覽的檔案上傳、進度條以及成功畫面，並嚴格遵循 ECOCO 的品牌視覺 (綠色 #00A94F、白、灰)。
---

# ECOCO 高級客服表單設計規範 (ECOCO Advanced Customer Form)

## 🎯 核心目標
建立一個具有高品質、動態互動且符合 ECOCO 品牌視覺的客服表單，使使用者在回報問題時能有極佳的專屬品牌體驗。

## 🎨 設計系統 (Design System)
- **品牌主色 (Primary Color)**: `#00A94F` (ECOCO Green)
- **背景色 (Background)**: 純白 `#FFFFFF` 或淺灰 `#F5F7FA`
- **文字顏色 (Text)**: 深灰 `#333333`、次要文字 `#666666`
- **邊框色 (Border)**: `#E2E8F0`
- **字體 (Typography)**: 優先使用系統無襯線字體或 `Inter`, `Roboto`, `Noto Sans TC`。
- **動態效果 (Micro-animations)**: Hover 效果需平滑過渡 (transition: 0.3s)，按鈕需有下壓或陰影變化。

## ⚙️ 核心功能需求 (Features)
1. **工單編號自動產生**: 格式為 `TK-YYYYMMDD-XXX` (例如：TK-20260416-001)，進入表單時自動賦予。
2. **會員資料自動帶入**: 預設帶入帳號與 Email (可編輯或唯讀模式設定)。
3. **階層式可搜尋下拉選單**:
   - 第一層：主要問題分類 (如：機台故障、點數問題、帳號問題、其他)。
   - 第二層：當選擇「機台故障」時，顯示站點搜尋框 (可輸入關鍵字快速篩選各機台據點)。
4. **檔案上傳與即時預覽**: 支援拖曳上傳 (Drag & drop)，並即時顯示圖片預覽縮圖，且可手動刪除預覽圖。
5. **進度時間軸 (Progress Timeline)**: 分階段引導使用者填寫 (例如：Step 1 驗證資料 -> Step 2 問題描述 -> Step 3 附件上傳)。
6. **成功送出畫面**: 包含動態打勾動畫、感謝訊息及專屬工單追蹤說明。

## 🛠 開發指引 (Implementation Guidelines)
- **HTML**: 使用完整的語意化標籤，確保不同裝置的適應性與無障礙存取 (Accessibility)。
- **CSS**: 優先使用 Vanilla CSS 或具備充分設定的 Tailwind，善用 Flexbox / CSS Grid 排版。按鈕與卡片需具備圓角 (`border-radius: 8px` 到 `16px`) 以及符合現代質感的陰影 (`box-shadow`)。
- **JavaScript**: 負責邏輯處理 (包含進度條切換、表單防呆驗證、圖片預覽渲染、下拉連動與即時搜尋)。確保 JS 邏輯模組化且易於後續維護。
