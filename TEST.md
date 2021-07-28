---
title: 製作一份自己的 Typora Theme
tags: ComputerScience.CSS
author: TpKotoba
---

# Test 測試

[TOC]

## 文字測試

### Lipsum

Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

> The quick brown fox jumped over the lazy dog.

This is the second paragraph. Hello, here is some text without a meaning. This text should show what a printed text will look like at this place. If you read this text, you will get no information. Really? Is there no information? Is there a difference between this text and some nonsense like not at all! A blind text like this gives you information about the selected font, how the letters are written and an impression of the look. This text should contain all letters of the alphabet and it should be written in of the original language. There is no need for special content, but the length of words should match the language.

### Font: Computer Modern

This package was compiled by Christian Perfect (http://checkmyworking.com) from the Computer Modern Unicode fonts created by Andrey V. Panov (http://cm-unicode.sourceforge.net/)

They're released under the SIL Open Font License. See OFL.txt and OFL-FAQ.txt for the terms.

A demo page for these fonts was at http://www.checkmyworking.com/cm-web-fonts/ when I released them. I can only apologise, citizen of the future, if that address doesn't exist any more.

### 字體：源流明體

「源流明體」是基於 [思源宋體](https://github.com/adobe-fonts/source-han-serif/) 的而改造的開放原始碼中文字型。

漢字寬度稍微壓縮，顯得比原始的思源宋體要稍微瘦長。 並且在橫筆的起筆與豎筆的起筆、收筆處，全都加上粗細變化。 彷彿重現鉛字的壓印感，文字較有文學感、人文氣息。

> Note. 請注意以上改造乃以電腦程式自動進行，未進行任何人工處理，在部分筆畫複雜文字可能會有筆畫不太一致的情況。

#### 傳統印刷體風格

思源宋體預設的台灣版本（TW）採用教育部標準字體，雖然適合教育用途，但不盡符合傳統印刷體審美觀。例如點、挑、撇筆畫太多，文件排列時的的跳動感較大。 此專案採用KR版本的字符為主，較接近傳統印刷體習慣，排列感較為整齊。

> Note: 本專案並沒有造新的字符，所有字符都是來自思源宋體本身。所以KR版本未收錄的罕用字或簡化字，仍然會是TW、CN風格。

#### 字體授權

- 本字型是基於 SIL Open Font License 1.1 改造Adobe所開發、發表的「[思源宋體](https://github.com/adobe-fonts/source-han-serif/)」字型。
- 本字型亦基於 SIL Open Font License 1.1 授權條款免費公開，關於授權合約的內容、免責事項等細節，請詳讀 License 文件。
  - 本字型可自由使用在印刷、影像、網路或任何媒體上，不限個人或商業使用。
  - 您可基於 SIL Open Font License 1.1 的規定再散佈或改造本字型。

## Block Elements

已經出現過的：paragraph, heading, blockquote, toc

---

### Unordered List

- 元素一
- 元素二
  - 元素二之一
  - 元素二之二
    - 元素二之二之一
    - 元素二之二之二
- 元素三

### Ordered list

1. 第一個項目
   1. 第一個子項目
   2. 第二個子項目
      1. 第一個孫項目
      2. 第二個孫項目
   3. 第三個子項目
2. 第二個項目

### Task list

- [ ] Task 1
- [x] Task 2

### Mathblocks and Quoteblocks

> Let $E$ be an elliptic curve defined by
>
> $$
> E:y^2 = x^3-x
> $$
>
> Enumerate
> $$
> E(\mathbb F_p):=\#\left\{(x, y)\in\mathbb F_p\times\mathbb F_p:y^2 = x^3-x\right\}\sqcup\{\infty\}
> $$
> when $p\equiv 1\,(\mathop{\rm mod}4)$. Surprisingly, it is related to integral solution to $x^2+y^2=p$.

#### Conclusion

We apply the sum of square partition to $p$:

$$
p = x^2+(2y)^2; x, y\in\mathbb N
$$
Then we have
$$
K(-1) = 2x\cdot(-1)^{(x+1)/2+y}
$$
**Note.** The value $-K(-1)=1+p-\#E$ is called *$p-$defect*, also called the *trace of Frobenius*.[^1]

##### 這裡放個五級標題來測試

###### 這裡放個六級標題來測試

[^1]: https://gohighbrow.com/elliptic-curves-and-modular-forms-a-1000000-mystery/

### Codeblocks

```css
:root{
	/* ==== 字體大小 ==== */
	/* 這裡的大小比例恰巧對應至宮商角徵羽；
	「……九九八十一以為宮。
    三分去一，五十四以為徵。
    三分益一，七十二以為商。
    三分去一，四十八以為羽。
    三分益一，六十四以為角。」
	──《史記》「律書第三」，司馬遷
	*/
	--h1-font-size: 2rem;
	--h2-font-size: 1.6875rem; /* 這個數字是 81/48 */
	--h3-font-size: 1.5rem; /* 這個數字是 81/54 */
	--h4-font-size: 1.265625rem; /* 這個數字是 81/64 */
	--h5-font-size: 1.111rem; /* 這個數字是 81/72 */
	--h6-font-size: 1rem;
}
```

### Table


| Column 1 | Column 2 | Column 3 |
| :------- | :------: | -------: |
| Left-aligned Content | Centered-aligned Content | Right-aligned Content |
| 內容靠左 | 內容置中 | 內容靠右 |

## Inline elements

Inline styles support **strong 加黑**, *emphasis 強調*, `Code or Keyboard 代碼或者鍵盤`, ~~strikethrough 刪除線~~, :smile:, X^2（上標）^, Y~2（下標）~, ==highlight 螢光筆==, [Link 連結](http://typora.io), [章節連結](#Inline elements), and image:[^footnote] <!--這個是註解，同樣 80% 尺寸--> 

![](https://typora.io/img/new/image.png)





[^footnote]: 這個是註腳  