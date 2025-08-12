# 使用說明與範例

[![BeautifulCommandLine](/Sample.PNG "BeautifulCommandLineSample")](https://github.com/OliverLiou/BeautifulCommandLine/Sample.PNG)

[![BeautifulCommandLine](/Sample2.PNG "BeautifulCommandLineSample2")](https://github.com/OliverLiou/BeautifulCommandLine/Sample2.PNG)

[![BeautifulCommandLine](/Sample3.PNG "BeautifulCommandLineSample3")](https://github.com/OliverLiou/BeautifulCommandLine/Sample3.PNG)

## **必要安裝與設定, 請先參考保哥教學**

[will保哥-如何打造一個華麗又實用的 PowerShell 命令輸入環境][01].

## Step1 根據文章說明, 請先建立自己的$PROFILE

## Step2 複製檔案

將 `oliver.omp.yaml` 檔案複製到 `C:\Users\{userName}\AppData\Local\Programs\oh-my-posh\themes`

注意: **{userName}** 請根據自己電腦環境命名

## Step3 執行使用主題指令

    oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\oliver.omp.yaml"  | Invoke-Expression

## Step4 執行命令加入到 $PROFILE 啟動設定檔中

    'oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH\oliver.omp.yaml"  | Invoke-Expression' | Out-File -LiteralPath $PROFILE -Append -Encoding utf8

<!-- link references -->
[01]: https://blog.miniasp.com/post/2021/11/24/PowerShell-prompt-with-Oh-My-Posh-and-Windows-Terminal
