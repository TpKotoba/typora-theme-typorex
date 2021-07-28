---
author: TpKotoba
---



# Typorex：一個偽裝成 TeX 的主題

[TOC]

這份佈景主題 fork 自 Github 上 [@Keldos-Li](https://github.com/Keldos-Li/) 所發佈的 「[Typora伪装LaTeX中文样式主题 typora-latex-theme](https://github.com/Keldos-Li/typora-latex-theme)」 項目，將其修改成易於臺灣學生使用的版本，並依照個人喜好將字體部份進行統一，整個版面看起來清新得多。該項目亦是建立在 [@让幻想飞](https://zhuanlan.zhihu.com/p/357096043) 與 [@LAN DU](https://zhuanlan.zhihu.com/p/158767474) 的貢獻上完成的。

> Note. 目前這份只是先行測試版，請盡量避免廣傳此項目。

作為一個誕生不到一週的 CSS 嬰兒，若是在程式碼上有考慮不周之處，望前輩們不吝指正。

## 安裝方法

1. 打開 Typora；
2. 在偏好設定裡面找到「外觀」，打開佈景主題資料夾；
3. 將 `typorex.css` 與 `typorex/` 放進去；
4. 重新啟動 Typora，就可以在外觀中選到 Typorex 了！

### 如果你習慣上不使用 h2 的話

將 `typorex.css` 中「h2 跳過系統」的第 588 與 634 行的註解標（`/*`, `*/`）去除即可。

## 外部資源使用

### 字體

中文：採用開源的「源流明體」：https://github.com/ButTaiwan/genryu-font。

> Note. 部份標點符號（比如引號「」）延續了思源宋體的陋習，只有 50% 字寬，望未來該字體能改善。

英文：TeX 系統原生的「Computer Modern Typewriter」，由 Christian Perfect 編譯：
https://www.checkmyworking.com/cm-web-fonts/。

### 顏色

許多的顏色取自「NIPPON COLORS 日本の伝統色」：https://nipponcolors.com。
