# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 專案概述

這是一個 Oh My Posh PowerShell 命令列美化配置專案，包含自訂主題檔案 `oliver.omp.yaml`。

## 架構說明

- **oliver.omp.yaml**: Oh My Posh 主題配置檔案，定義了命令列提示符的外觀和功能
- **README.md**: 安裝和使用說明
- **CLAUDE.md**: Claude Code 操作指引

## Oh My Posh 主題結構

主題檔案 `oliver.omp.yaml` 包含以下主要區段：
- **OS 指示器**: 顯示作業系統圖示
- **電池狀態**: 顯示電池電量和充電狀態（包含彩色指示和圖示）
- **路徑顯示**: 當前工作目錄，採用資料夾圖示風格
- **Git 狀態**: 顯示 Git 分支和狀態資訊
- **.NET SDK 版本**: 當有 .NET 專案時顯示 SDK 版本
- **Node.js 版本**: 當有 Node.js 專案時顯示版本
- **Root 用戶指示器**: 當以管理員身分執行時顯示
- **命令執行時間**: 顯示上一個命令的執行時間（超過 500ms 才顯示）

## 常用命令

### 安裝主題
```powershell
# 複製主題檔案到 Oh My Posh themes 目錄
Copy-Item oliver.omp.yaml "$env:POSH_THEMES_PATH\"

# 初始化主題（臨時使用）
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\oliver.omp.yaml" | Invoke-Expression

# 永久設定（加入到 PowerShell 設定檔）
'oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\oliver.omp.yaml" | Invoke-Expression' | Out-File -LiteralPath $PROFILE -Append -Encoding utf8
```

### 測試和開發
```powershell
# 測試主題配置
oh-my-posh config export --config oliver.omp.yaml --format json

# 驗證配置檔案
oh-my-posh debug --config oliver.omp.yaml
```

## 設定注意事項

- 需要先安裝 Oh My Posh 和支援的字體（如 Nerd Fonts）
- 配置檔使用 YAML 格式，修改時注意縮排
- 顏色配置使用十六進制色碼
- 圖示需要 Nerd Fonts 支援

## 回應語言設定

請使用繁體中文（zh-TW）回應。