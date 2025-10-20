# CSV 資料圖表顯示器

## 📋 功能特色

- 📊 支援 CSV 檔案上傳與即時視覺化
- 🎯 多種滑鼠懸停模式（最近數據、X/Y Marker）
- 📏 自訂 X/Y 軸範圍
- ✏️ 可編輯圖表標題（雙擊標題）
- 💾 另存為獨立 HTML 檔案
- 📸 匯出高解析度 JPG 圖片（1920×1080）
- 🎨 自動識別 spec 欄位（粉紅色虛線顯示）

## 🚀 使用方式

**線上版本：**[https://kevinzheng81.github.io/csv_plotter_webapp/csv_plotter_webapp.html](https://kevinzheng81.github.io/csv_plotter_webapp/csv_plotter_webapp.html)

**離線使用：**下載 HTML 檔案，用瀏覽器開啟即可

## 📝 CSV 格式要求

### 標準格式
```csv
X軸標籤,曲線1名稱,曲線2名稱,...,Y軸標籤
X值1,Y值1-1,Y值1-2,...,
X值2,Y值2-1,Y值2-2,...,
```

### 範例
```csv
Frequency (GHz),1L_1R (dB),2L_2R (dB),PCIE6_spec,dB
0.01,-0.0174,-0.0146,-10,
0.02,-0.0001,-0.0093,-10,
0.03,0.0107,0.0202,-10,
```

**說明：**
- 第一列為標題（第一欄 = X軸，最後一欄 = Y軸，中間 = 各曲線名稱）
- 數據列最後一欄可留空
- 包含 "spec" 的曲線會自動以粉紅色虛線顯示

## 💻 技術說明

- 純前端應用，所有資料處理都在本地完成
- 使用 Plotly.js 2.27.0 和 PapaParse 5.4.1
- 支援 Chrome、Edge、Firefox、Safari

---

**最後更新：** 2025年10月
