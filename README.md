# 司法院裁判書結構化與開放資料
Judicial_Judgements

# 計畫目的

- 建立司法裁判書結構化架構
- 採用 [Akoma Ntoso](http://www.akomantoso.org/) 架構 - 建立司法裁判書交換格式
- 建立判決書瀏覽器 + 網頁外掛
- 判決書資料分析

## 說明

司法院在 2017.03.22 於 http://data.gov.tw/ 網站上釋出了 2016 全年的裁判書開放資料集 ([司法院新聞稿](http://jirs.judicial.gov.tw/GNNWS/NNWSS002.asp?id=259695))。資料集的內容依照月份，法庭做分類，每一份裁判書則是一個獨立的 json 檔。

```json
{
  "JID":"SJEM,104,重秩聲,17,20160126,1",
  "JYEAR":"104",
  "JCASE":"重秩聲",
  "JNO":"17",
  "JDATE":"20160126",
  "JTITLE":"違反社會秩序維護法",
  "JFULL":"臺灣新北地方法院三重簡易庭裁定　　 104年度重秩聲字第17號\r\n
           移送機關　　新北市政府警察局新莊分局\r\n
           ...
           十一、綜上，原處分機關據以援引上開規定，各裁處罰鍰9,000\r\n
                元，及沒入共同賭資，並無不當。\r\n
           十二、爰依社會秩序維護法第57條第2項前段，裁定如主文。\r\n
           中    華    民    國     105    年    1     月    26   日\r\n
           臺灣新北地方法院三重簡易庭\r\n
           法  官  吳智勝\r\n
           以上正本係照原本作成。\r\n
           本件不得抗告。\r\n
           中    華    民    國     105    年    1     月    26   日\r\n
           書記官  葉子榕"           
}
```

從現在釋出的版本，可以看到裁判書本身的結構化程度不足，內容排版不佳，同時也缺乏與原文（裁判書搜尋網站）的連結。也就是要作為一個實用性較高的資料內容，還須要進一步對內容拆解與更好的結構化。


# 相關連結

1. [司法院](http://www.judicial.gov.tw/)
2. [裁判書查詢](http://jirs.judicial.gov.tw/FJUD/FJUDQRY01M_1.aspx)
3. [法學資料檢索系統](http://jirs.judicial.gov.tw/Index.htm)
4. [裁判書開放資料](http://data.gov.tw/wise_search?nodetype=metadataset&kw=%E8%A3%81%E5%88%A4%E6%9B%B8) - data.gov.tw


# 其他計畫

## 臺灣
1. [法拍屋 parser](https://github.com/shadowjohn/judicial)
2. [裁判書小幫手](https://github.com/ronnywang/judicial-easyer) [網站](http://judicial.ronny.tw/)- ronnywang
3. [判決書懶人包 - 摘要編輯器](https://github.com/ctiml/judicial-summary)
3. [司法院爬蟲](https://github.com/biglawtw/judicial_crawler) - biglawtw
4. [司改國是會議](https://github.com/JRF-tw/nationwide_judicial_reform_meeting) - 司改會

## 其他
1. [Free Law Project](https://free.law/) | [Github](https://github.com/freelawproject)
2. [Judgements API](https://github.com/openva/judgmental)

# 參考資料
- [Legislative XML for the Semantic Web: Principles, Models, Standards for Document Management](https://play.google.com/store/books/details/Giovanni_Sartor_Legislative_XML_for_the_Semantic_W?id=2yBVDmy-MCkC)
- [LegalRuleML]
- [Atoma Ntoso]
- [ LegalXML]

Judicial.gov.tw - Judgements Open Data
