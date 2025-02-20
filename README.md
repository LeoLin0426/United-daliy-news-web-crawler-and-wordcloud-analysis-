# 爬取聯合新聞網每日所有新聞並進行文本分析
每日新聞資訊量龐雜，如何在有限時間下快速從中提取關鍵資訊是一個挑戰。以本專案為例，光是聯合新聞網，每天就產出高達400+的新聞內容。為了使獲得資訊更有效率，我們寫出這個用於爬取新聞數據並生成文字雲的工具，它通過Ajax動態載入網頁，爬取新聞內容並擷取標題，將其保存為CSV文件。此外，再利用`jieba`進行文本分析，生成文字雲圖片。
它可以幫助我們迅速掌握近期的熱門議題，從而更高效地把握資訊動態。這種工具不僅適用於新聞領域，還可以廣泛應用於其他多個領域，如：
- 行業分析：抓取某行業的所有財報會議記錄，分析其中最流行的關鍵詞，幫助我們快速了解行業趨勢和市場動態。
- 政策分析：抓取政府公告或政策文件中的關鍵詞，幫助研究人員或從業者快速把握政策導向和重點。
- 社交媒體監控：分析特定話題或品牌的社交媒體帖子，提取熱門關鍵詞，用於品牌管理和輿情分析。
- 客戶服務：分析客戶反饋或評論中的關鍵詞，了解客戶需求和痛點，優化產品和服務。

## 功能特點

1. **動態網頁爬取**：模擬網頁滾動加載，爬取動態加載的新聞數據。
2. **數據保存**：將爬取的新聞數據保存為CSV文件，供使用者進行額外分析。
3. **文字雲生成**：提取新聞標題，生成文字雲圖片。
4. **停用詞過濾**：支持自定義停用詞，過濾無意義的詞彙。

## 使用方法
1. **安裝相關套件:**
```
pip install requests pandas jieba wordcloud matplotlib pillow
```
2. **下載生成文字雲所需字體:**
    - [點此下載](https://www.techmarks.com/chinese-font-download/)或使用倉庫中使用所附之字體(ttf檔)
    - 下載完成後記住檔案存檔路徑

3. **在程式之Cell 5中設定好字體檔案路徑**
4. **執行程式檔，跑出文字雲，並可將爬取之新聞輸出成csv檔。**
## 文字雲結果呈現
<img src="wordcloud.png" width="60%" />
