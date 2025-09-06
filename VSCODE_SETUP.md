# 🎯 VS Code / Cursor 完整開發環境設定

本文檔說明為 OpenIM Flutter Demo 專案建立的完整 VS Code/Cursor 開發環境配置。

## 📁 配置文件概覽

### `.vscode/` 目錄結構

```
.vscode/
├── launch.json        # 除錯配置
├── tasks.json         # 任務配置
├── settings.json      # 工作區設定
├── extensions.json    # 推薦擴充功能
└── keybindings.json   # 自訂快捷鍵
```

## 🚀 除錯配置 (launch.json)

### 主要除錯配置

- **🚀 OpenIM Demo (Debug)** - 標準除錯模式
- **🔧 OpenIM Demo (Debug - Android)** - Android 設備除錯
- **🍎 OpenIM Demo (Debug - iOS)** - iOS 設備除錯
- **🏃 OpenIM Demo (Profile)** - 效能分析模式
- **🚀 OpenIM Demo (Release)** - Release 模式
- **🌐 OpenIM Demo (Web)** - Web 平台除錯
- **🧪 OpenIM Demo (Tests)** - 測試除錯

### 進階配置

- **📱 OpenIM Demo (指定設備)** - 動態選擇設備
- **🔍 OpenIM Demo (除錯模式 + 詳細日誌)** - 詳細除錯
- **⚡ OpenIM Demo (熱重載)** - 熱重載模式
- **🎯 OpenIM Demo (特定入口點)** - 自訂入口點

### 複合配置

- **🔄 同時啟動 Android 和 iOS** - 多平台同步除錯
- **🧪 測試 + 除錯** - 測試與除錯組合

## 🛠️ 任務配置 (tasks.json)

### 快速任務

- **🚀 啟動應用程式** - `Cmd+R`
- **🔧 Debug 模式運行** - `Cmd+Shift+R`
- **📱 構建 Android APK** - `Cmd+B`
- **🚀 構建 Release APK** - `Cmd+Shift+B`

### 開發任務

- **🧪 執行測試** - `Cmd+T`
- **📊 執行測試 (含覆蓋率)** - `Cmd+Shift+T`
- **🔍 程式碼分析** - `Cmd+L`
- **✨ 格式化程式碼** - `Cmd+Shift+F`
- **🧹 清理專案** - `Cmd+K Cmd+C`

### 構建任務

- **🍎 構建 iOS 應用**
- **📦 更新依賴**
- **🔨 生成程式碼**
- **⚙️ 初始化開發環境**

### 調試任務

- **🔄 熱重啟**
- **🔧 附加到進程**
- **📱 連接到 Android 設備**
- **🍎 連接到 iOS 設備**
- **🌐 在 Web 上運行**
- **🚀 Profile 模式運行**

## ⚙️ 工作區設定 (settings.json)

### Flutter/Dart 設定

```json
{
  "dart.debugExternalPackageLibraries": true,
  "dart.lineLength": 120,
  "dart.closingLabels": true,
  "dart.previewFlutterUiGuides": true,
  "dart.flutterSelectDeviceWhenConnected": true
}
```

### 程式碼格式化

```json
{
  "editor.formatOnSave": true,
  "editor.formatOnType": true,
  "editor.codeActionsOnSave": {
    "source.fixAll": "explicit",
    "source.organizeImports": "explicit"
  }
}
```

### 檔案排除設定

- 自動排除 `build/`, `.dart_tool/`, `Pods/` 等目錄
- 優化搜尋和檔案監視效能

### 終端機環境

- 自動將 `scripts/` 目錄加入 PATH
- 跨平台支援 (macOS, Linux, Windows)

## 📦 推薦擴充功能 (extensions.json)

### 必需擴充功能

- **dart-code.dart-code** - Dart 語言支援
- **dart-code.flutter** - Flutter 框架支援

### 開發工具

- **ms-vscode.vscode-json** - JSON 支援
- **redhat.vscode-yaml** - YAML 支援
- **davidanson.vscode-markdownlint** - Markdown 檢查

### Git 和版本控制

- **github.vscode-pull-request-github** - GitHub 整合
- **eamodio.gitlens** - Git 歷史檢視

### 實用工具

- **christian-kohler.path-intellisense** - 路徑自動完成
- **wayou.vscode-todo-highlight** - TODO 高亮
- **gruntfuggly.todo-tree** - TODO 樹狀檢視

## ⌨️ 快捷鍵配置 (keybindings.json)

### 主要快捷鍵

| 快捷鍵        | 功能                | 說明         |
| ------------- | ------------------- | ------------ |
| `Cmd+R`       | 啟動應用程式        | 非除錯模式下 |
| `Cmd+Shift+R` | Debug 模式運行      | 除錯啟動     |
| `Cmd+B`       | 構建 Android APK    | 快速構建     |
| `Cmd+Shift+B` | 構建 Release APK    | 發布構建     |
| `Cmd+T`       | 執行測試            | 基本測試     |
| `Cmd+Shift+T` | 執行測試 (含覆蓋率) | 完整測試     |
| `F5`          | 開始除錯            | 標準除錯     |
| `Shift+F5`    | 停止除錯            | 結束除錯     |

### Flutter 特定快捷鍵

| 快捷鍵              | 功能           | 說明      |
| ------------------- | -------------- | --------- |
| `Cmd+K Cmd+R`       | 熱重載         | 即時更新  |
| `Cmd+K Cmd+Shift+R` | 熱重啟         | 重新啟動  |
| `Cmd+K Cmd+P`       | 開啟 DevTools  | 開發工具  |
| `Cmd+K Cmd+I`       | 顯示 Inspector | UI 檢查器 |

### 專案特定快捷鍵

| 快捷鍵  | 功能         | 說明         |
| ------- | ------------ | ------------ |
| `Cmd+1` | Debug 模式   | 標準除錯     |
| `Cmd+2` | Android 除錯 | Android 設備 |
| `Cmd+3` | iOS 除錯     | iOS 設備     |
| `Cmd+4` | Web 除錯     | Web 平台     |

## 🚀 快速開始使用

### 1. 開啟專案

```bash
# 使用 VS Code
code .

# 使用 Cursor
cursor .
```

### 2. 安裝推薦擴充功能

1. 開啟 VS Code/Cursor
2. 會自動提示安裝推薦擴充功能
3. 點擊 "Install All" 安裝全部

### 3. 開始除錯

1. 按 `F5` 或點擊除錯圖示
2. 選擇 "🚀 OpenIM Demo (Debug)"
3. 等待應用程式啟動

### 4. 設定中斷點

1. 在程式碼行號左側點擊
2. 紅點表示中斷點已設定
3. 除錯時會在該點停止

## 🔧 自訂配置

### 修改快捷鍵

1. 開啟 `.vscode/keybindings.json`
2. 修改 `key` 欄位
3. 儲存檔案即生效

### 新增除錯配置

1. 開啟 `.vscode/launch.json`
2. 在 `configurations` 陣列中新增配置
3. 設定名稱、類型、程式等參數

### 新增任務

1. 開啟 `.vscode/tasks.json`
2. 在 `tasks` 陣列中新增任務
3. 設定標籤、命令、參數等

## 📋 常見問題

### Q: 除錯時找不到設備？

**A**:

1. 執行 `./scripts/app.sh dev devices` 檢查設備
2. 確保設備已連接且啟用開發者模式
3. 重新啟動 VS Code/Cursor

### Q: 熱重載不工作？

**A**:

1. 確保在除錯模式下運行
2. 使用 `Cmd+K Cmd+R` 手動觸發熱重載
3. 檢查是否有編譯錯誤

### Q: 任務執行失敗？

**A**:

1. 檢查腳本權限：`chmod +x scripts/*.sh`
2. 確保 Flutter 環境正常：`flutter doctor`
3. 查看任務輸出的錯誤訊息

### Q: 擴充功能無法安裝？

**A**:

1. 檢查網路連接
2. 重新啟動 VS Code/Cursor
3. 手動搜尋並安裝擴充功能

## 🎯 最佳實踐

### 除錯流程

1. **設定中斷點** - 在關鍵位置設定
2. **啟動除錯** - 使用 F5 或除錯面板
3. **檢查變數** - 在變數面板中查看
4. **單步執行** - 使用 F10/F11 逐步檢查
5. **使用監視** - 監視重要變數變化

### 開發流程

1. **環境檢查** - `make doctor`
2. **程式碼開發** - 編寫功能
3. **即時測試** - 熱重載檢視效果
4. **程式碼檢查** - `make check`
5. **執行測試** - `make test-all`
6. **構建發布** - `make release`

### 效能優化

1. **排除不必要的檔案** - 設定 `files.exclude`
2. **使用工作區設定** - 避免全域設定衝突
3. **定期清理** - `make clean` 清理暫存
4. **監控記憶體** - 關注除錯時記憶體使用

這個完整的開發環境配置將大大提升您的 Flutter 開發效率！🚀
