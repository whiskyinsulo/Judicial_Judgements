# 司法院裁判書結構化與開放資料
Judicial_Judgements

## 前言

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
           ..."
}
```

# 相關連結

1. [司法院](http://www.judicial.gov.tw/)
2. [裁判書查詢](http://jirs.judicial.gov.tw/FJUD/FJUDQRY01M_1.aspx)
3. [法學資料檢索系統](http://jirs.judicial.gov.tw/Index.htm)


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



Judicial.gov.tw - Judgements Open Data
