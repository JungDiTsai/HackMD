<!-- {%hackmd EafFu4VWQKuKkTQQXbkxGg %} -->
# 前端讀書會-Introduce
[toc]
## Introduce
### What we usually do ?
:::info
1. HTML: 表述並定義內容。(傳遞內容)
2. CSS: 用來描述網頁的外觀(美化外觀)。
3. JavaScript: 功能性的程式語言(與使用者的交互行為)
:::
---

## HTML5
來源連結:[HTML-MDN](https://developer.mozilla.org/zh-TW/docs/Web/HTML)、[HTML元素](https://zh.wikipedia.org/wiki/HTML%E5%85%83%E7%B4%A0)
1) What is HTML ?
:::info
1. HTML的全名是-HyperText Markup Language。
    1) Hypertext(超文本)，是一種可以顯示在電子裝置上的文字。目前普遍以電子文件的方式存在，其中的文字包含有可以連結到其他欄位或者文件的超連結，允許從當前閱讀位置直接切換到超連結所指向的文字。
    2) Markup (標記)-用來詮釋文字、突現、其他能在瀏覽器顯示的內容。HTML 標記還包括一些特殊「元素」（element），例如： 
    ```html=
    <head>、<title>、<body>、<header>、<footer>、
    <article>、<section>、<p>、<div>、<span>、<img>...等等
    ```
    3) HTML 文件中的元素和其他內容文字不同的地方，在於元素名稱本身用「<」與「>」包圍，稱作「標籤」。HTML 標籤不分英文大小寫。也就是說，它們可以寫成英文全大寫、全小寫、或是混在一起。
    4) HTML 標籤都是成對的，而且是「巢狀」的結構。但一些元素如換行符 < br >，不允許嵌入任何內容，無論是文字或其他標籤。這些元素只需一個單一的空標籤（類似於一個開始標籤），無需結束標籤。

< h1 >
    < h2> < /h1 >
< /h2>
:::
### css3
來源連結:[CSS-MDN](https://developer.mozilla.org/zh-TW/docs/Web/CSS)
1) What is HTML ?
:::info
層疊樣式表(Cascading Style Sheets, CSS)，是用來描述 HTML 或 XML（包含 SVG 或 XHTML 等各種 XML 變形）文件外觀的樣式表語言。CSS 會描述文件裡的結構化元素，該如何呈現在螢幕、紙、語音報讀、或其他媒介上。
:::
### JavaScript
來源連結: [JavaScript-MDN](https://developer.mozilla.org/zh-TW/docs/Web/JavaScript)
:::info
JavaScript (簡稱 JS) 是具有"[**一級函術**](https://zh.wikipedia.org/wiki/%E5%A4%B4%E7%AD%89%E5%87%BD%E6%95%B0)"(First-class functions) 的輕量級、==直譯式==或即時編譯（JIT-compiled）的程式語言。它因為用作網頁的腳本語言而大為知名，但也用於許多非瀏覽器的環境，像是 node.js、Apache CouchDB。JavaScript 是一個基於原型的 (Prototype-based)、多範型的、動態語言，支援物件導向、指令式以及宣告式 (如函數式程式設計) 風格。 
:::

---

## 在一個網頁裡的結構
:::info
- ==<!DOCTYPE html>==:告訴瀏覽器這份文件是一個 HTML5 的網頁，瀏覽器因而知道要怎麼用正確的方式來展示你的網頁。請注意宣告要寫在第一行，因為瀏覽器是一行一行讀取文件的，想愈早告訴他的資訊，請寫在愈上面。
- == < html >< /html > == 此標籤是置於整個文件的開始和結束之處，以供瀏覽器識別此文件為合法的文件。
- == < head >< /head > ==包圍的資訊稱為「標頭」，<head> 裡宣告各種網頁資訊，這些資訊不會顯示給使用者看，因為它們的溝通對象是瀏覽器與其他的網路服務，如 Google 搜索引擎，Facebook 等。<head> 宣告的資訊包括網頁標題、外部連結、網頁樣式、JavaScript 腳本、meta tag⋯⋯等。
- head tag 
- ==<title></title>==:此標籤中的就是此網頁的標題，也就是您瀏覽器最左上面的標題，若沒設則只會顯示成此網頁所在的網址。
- ==<body></body>==:此標籤中所寫的內容即會顯示於網頁裡面，至於裡面要寫些什麼、可以寫些什麼，以我就會教你們怎麼去寫自己的網頁了。
:::

### 基本網頁元素
:::info
- 標題：h1, h2, h3, h4, h5, h6
- 文字段落：p
- 清單：ul, ol, li
- 強調語氣：em, strong
- 換行：br
- 水平線：hr
- 超連結：a
- 圖片：img
- 區域：div, span
- 表格：table, tr, th, td
- 表單：form, label, input
除了 img 標籤外，header、nav、main 和 section 是==語義元素== (semantic element)，也就是「有意義的元素」，能讓搜尋引擎辨識出正確的網頁內容。
- 空元素一覽表: https://developer.mozilla.org/zh-TW/docs/Glossary/Empty_element
:::

### 範例:
```htmlmixed=
<!DOCTYPE html>
<html lang="en">
    <!-- lang="en" 便是沒有特定的地區 -->
<head>
    <!-- 主要放置得標籤用來告訴搜尋引擎這個網頁有什麼樣的內容、控制網頁與外部程式碼的連結、
        定義網頁使用的樣式等等(例如你的css檔如何跟html運作)<title>、<meta>、<link>、<script>、<style>、<base>  -->
    <meta charset="UTF-8">
        <!-- 在 head 標籤內，表示要適應各種網路瀏覽器的編碼問題，
        如：IE瀏覽器預設文字編碼是BIG-5，我們在這邊先宣告統一使用utf-8編碼，解決使用不同瀏覽器會看到亂碼的問題。 
    -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name=COPYRIGHT content="Copyright (c) by Jung ">
    <!-- 註明版權所有 -->
    <meta name="description" content="全台最大3C零件銷售平台、舉凡電腦、手機、平板都買的到">
    <!-- 搜尋引擎都會以網頁的前廿五字做為網頁內容摘要 -->
    <title>Welcome Everyone</title>
    <!-- style標籤是我們可以放寫Css的地方(classname) -->
    <style>
        .message-box{
            width: 200px;
            height: fit-content;
            display: none;
            border: 1px solid green;
            border-radius: 5px;
            text-align: center;
            margin: auto ;
        }
        .protect{
            position: fixed;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            width: 100%;
            height: 100%;
            background-color: #ddd;
        }
        #close{
            position:relative;
            z-index: 1;
            cursor: pointer;
        }

        table {
        border-collapse: collapse;
        }

        table, th, td {
        border: 1px solid black;
        }
    </style>
    
</head>
<!-- body 包圍的內容是會直接顯示給使用者看的內容，也是這個網頁的核心。需要 CSS 來定義樣式的內容，也都會放在 body 裡面，現在，請你立刻在 body 裡輸入以下內容  -->
<body>
    <!-- 這裡是傳統的寫法 -->
    <div class="header"></div>
        <div class="nav"></div>
        <div class="main">
            <div class="article"></div>
            <div class="aside"></div>
        </div>
        <div class="footer">
            Updated on <span class="time"></span>
    </div>
    <a href="https://google.com">Google</a>
    <img src="https://www.google.com/logos/doodles/2015/googles-new-logo-5078286822539264.3-hp2x.gif" alt="GOOGLE">
    <br>
    <hr>
    <ol>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ol>
    <ul>
        <li>1</li>
        <li>2</li>
        <li>3</li>
    </ul>
    <table>
        <thead>
            <tr>
                <th>cats</th>
                <th>dogs</th>
            </tr>
        </thead>
        
        <tbody>
            <tr>
                <td>7</td>
                <td>6</td>
            </tr>
        </tbody>
        
        <tfoot>
            <tr>
                <th colspan="2">Cats win!</th>
            </tr>
        </tfoot>
    </table>
    <table>
        <tr>
            <th>Month</th>
            <th>Savings</th>
            <th>Savings for holiday!</th>
        </tr>
        <tr>
            <td>January</td>
            <td>$100</td>
            <td rowspan="2">$50</td>
        </tr>
        <tr>
            <td>February</td>
            <td>$80</td>
        </tr>
      </table>
    <!-- 這裡是使用語意標籤和 <div>、<span> 一樣，沒有預設樣式。 -->

    <!-- nav 網頁的選單與導覽 -->
    <nav >網頁的選單、導覽</nav>
    <!-- main 網頁的主要內容 -->
    <!--   元素內的內容對於文檔應該是唯一的。它不應包含跨文檔重複的任何內容，例如側欄，導航鏈接，版權信息，網站徽標和搜索表單。同時它不能是<article>，<aside>，<footer>，<header>或<nav>元素的後代。 //20200722  -->
    <main style="border: 1px solid blue;">
        <!-- article 一篇文章內容 -->
        <article>
            <!-- section 自訂的區塊，例如數篇摘要組成的空間。-->
            <section>
                <div>
                    <h2>電腦零件</h2>
                    <p>硬碟、記憶體、螢幕</p>
                </div>
            </section>
            <section>
                <div>
                    <h2>手機零件</h2>
                    <p>保護貼、手機殼、電源線</p>
                </div>
            </section>
        </article>
        <aside>：網頁的側欄、附加內容。</aside>
    </main>
    <!-- footer 網頁的頁尾，通常放置聯絡方式、著作權宣告等等。 -->
    <footer>
        <!-- time 顯示日期時間 -->
        網頁的頁尾，通常放置聯絡方式、著作權宣告等等。Updated on <time></time>
    </footer>
    <button id="message-button">打開 message Box</button>
    <div id="message" class="message-box">
        <div class="protect"></div>
        <button id="close">關閉</button>
    </div>
    
    <script>
        window.onload = function () {
            let messageButton = document.getElementById('message-button')
            let close = document.getElementById('close')
            messageButton.addEventListener("click", toggleMessageBox)
            close.addEventListener("click", toggleMessageBox)
        }
    
        function toggleMessageBox() {
            let status = document.getElementById('message').style.display
            console.log( document.getElementById('message').style.display)
            if (status === 'block') {
                document.getElementById('message').style.display = 'none'       
            } else {
                document.getElementById('message').style.display = 'block'       
            }
            // status === 'block' ? document.getElementById('message').style.display = 'none' :document.getElementById('message').style.display = 'block'
            // 這一段是三元運算式
        }
    </script>
</body>
</html>
```



###### tags: `前端讀書會`