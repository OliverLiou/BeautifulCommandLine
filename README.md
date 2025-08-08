# 根據文章指示, 請先建立自己的$PROFILE

# 1.將檔案複製到 C:\Users\{userName}\AppData\Local\Programs\oh-my-posh\themes

# .使用主題
    ```powershell
    oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\oliver.omp.yaml"  | Invoke-Expression
    ```

# .執行命令加入到 $PROFILE 啟動設定檔中
    ```powershell
    'oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\oliver.omp.yaml"  | Invoke-Expression' | Out-File -LiteralPath $PROFILE -Append -Encoding utf8
    ```

# 安裝詳細步驟請參考以下網址
    [will保哥-如何打造一個華麗又實用的 PowerShell 命令輸入環境]
    (https://blog.miniasp.com/post/2021/11/24/PowerShell-prompt-with-Oh-My-Posh-and-Windows-Terminal)