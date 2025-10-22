# CSV 資料圖表顯示器

## 📋 功能特色

- 📊 支援 CSV 檔案上傳與即時視覺化
- 🎯 多種滑鼠懸停模式（最近數據、X/Y Marker）
- 📐 支援線性/對數座標軸切換
- 📏 自訂 X/Y 軸範圍（X 軸支援 SI 單位前綴：m, u, n, p）
- ✏️ 可編輯圖表標題（雙擊標題）
- 💾 另存為獨立 HTML 檔案
- 📸 匯出高解析度 JPG 圖片（1280×720）
- 🎨 自動識別 spec 欄位（粉紅色虛線顯示）

## 🚀 使用方式

### 線上版本

- **基本版：** [https://kevinzheng81.github.io/csv_plotter_webapp/csv_plotter_webapp.html](https://kevinzheng81.github.io/csv_plotter_webapp/csv_plotter_webapp.html)
- **對數座標版：** [https://kevinzheng81.github.io/csv_plotter_webapp/csv_plotter_webapp_with_log.html](https://kevinzheng81.github.io/csv_plotter_webapp/csv_plotter_webapp_with_log.html)

### 離線使用

下載 HTML 檔案，用瀏覽器開啟即可使用。

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

### 說明

- 第一列為標題（第一欄 = X軸，最後一欄 = Y軸，中間 = 各曲線名稱）
- 數據列最後一欄可留空
- 包含 "spec" 的曲線會自動以粉紅色虛線顯示

## 🎨 座標軸類型（對數座標版限定）

**對數座標版**支援 X/Y 軸分別切換為：

- **線性軸：** 一般等間距刻度（10, 20, 30, 40...）
- **對數軸：** 以 10 的次方顯示（10⁰, 10¹, 10², 10³...）
  - 主刻度：10 的整數倍數
  - 次要網格線：提供更細緻的刻度參考

適合用於頻域分析、阻抗曲線、頻率響應等工程應用。

## 💻 技術說明

- 純前端應用，所有資料處理都在本地完成
- 使用 Plotly.js 2.27.0 和 PapaParse 5.4.1
- 支援 Chrome、Edge、Firefox、Safari

## 📄 授權

MIT License

---

**最後更新：** 2025 年 10 月
