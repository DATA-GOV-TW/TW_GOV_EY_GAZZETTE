# 行政院公報開放資料

行政院公報目前在每個發佈日會提供一個包含當日所有公報的 XML 檔案。這份 XML 檔案內容包含了如公報類型，發佈機關，發文日期，標題，主旨，關鍵字，內容（HTML 格式）等不同欄位。

# 資料來源

- [行政院公報資訊網](https://gazette.nat.gov.tw/egFront/index.do)

# 問題

- 內容 (HTMLContent) 包含 MS Words tag
- 所有內容都包在 !CDATA 內 
- 公告缺少直接對應到 Join 的連結
- 結構化，但是骯髒的內容
- 關鍵字感覺雜亂可怕

# 資料格式說明

[XML 範例](https://gazette.nat.gov.tw/egFront/fileView.do?fileType=openDataSamplePath&fileName=3680d08ac14c47e32eb51687046f4f79&attached)

## XML欄位說明
XML Tag|中文欄位|欄位內容範例及備註
|---|---|---|
|MetaId|公報系統流水號|60079<br>各則公報的PDF檔是以公報系統流水號命名，<br>如：流水號 60079 的公報其 PDF 檔是 60079.pdf|
|Doc_Style_LName|公報類型|法規|
|Doc_Style_SName|公報小類型|中央法規標準法第 3 條之 7 種命令<br>公報類型第二層|
|Chapter|公報篇別|衛生勞動篇<br>編輯分類 (篇名) 第一層|
|PubGov|公報小篇|衛生署<br>編輯分類 (篇名) 第二層|
|PubGovName|公(發)布機關|行政院衛生署|
|UndertakeGov|承辦機關|行政院衛生署食品藥物管理局|
|Officer_name|機關首長|署長 邱文達|
|Date_Created|發文日期|中華民國 102 年 4 月 9 日|
|GazetteId|發文字號|署授食字第 1021300776 號|
|Date_Published|刊登日期|中華民國 102 年 4 月 9 日|
|Comment_Deadline|表示意見截止日期|例：中華民國 102 年 6 月 9 日<br>只有草案預告才有欄位值|
|Comment_Days|預告天數|例：60<br>只有草案預告才有欄位值|
|Title|標題|行政院衛生署令：修正「食品器具容器包裝衛生標準」<br>第 5 條、第 6 條、第 7 條條文|
|TitleEnglish|英文標題|DEPARTMENT OF HEALTH, EXECUTIVE YUAN Order <br>is hereby given, for the amendment on Article 5, 6 and 7 <br>of "Sanitation Standard for Food Utensils, Containers and Packages"|
|ThemeSubject|主旨|修正「食品器具容器包裝衛生標準」第五條、第六條、第七條。|
|Keyword|關鍵字|食品容器;飲食衛生(食品衛生，營養衛生);食品安全(食品管理);<br>塑膠容器;食品器具;食品包裝;管制措施(限制措施);限量控管;幼兒;<br>嬰兒(新生兒);毒性化學物質;雙酚A|
|Eng_Keyword|英文關鍵字||
|Explain|說明|修正「食品器具容器包裝衛生標準」第五條、第六條、第七條。 <br>附修正「食品器具容器包裝衛生標準」第五條、第六條、第七條|
|Category|內容主題|830|
|Cake|施政分類|J32;B33<br>若有多個分類以;區隔|
|Service|服務分類||
|GazetteHTML|公報網址|指該則行政院公報的網址|
|HTMLContent|網頁內容|指該則行政院公報的網頁內容，請參考 XML 範例|

## 轉 JSON 檔
使用 XML OXHGEN 轉檔功能


