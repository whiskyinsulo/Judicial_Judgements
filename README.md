# 司法院裁判書結構化與開放資料
Judicial.gov.tw - Judgements Open Data

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

# ToDo
1. 判決書基礎架構與分類
2. 判決書結構標準
3. Parser - formatter - viewer
3. Atoma Ntoso XML 結構化

# 相關法令

## 刑事訴訟法
- [第 308 條](http://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=C0010001&FLNO=308) : 判決書應分別記載其裁判之主文與理由；有罪之判決書並應記載犯罪事實，且得與理由合併記載。
- [第 309 條]((http://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=C0010001&FLNO=309)) : 有罪之判決書，應於主文內載明所犯之罪，並分別情形，記載下列事項：
  1. 諭知之主刑、從刑、刑之免除或沒收。
  2. 諭知有期徒刑或拘役者，如易科罰金，其折算之標準。
  3. 諭知罰金者，如易服勞役，其折算之標準。
  4. 諭知易以訓誡者，其諭知。
  5. 諭知緩刑者，其緩刑之期間。
  6. 諭知保安處分者，其處分及期間。
- [第 310 條]((http://law.moj.gov.tw/LawClass/LawSingle.aspx?Pcode=C0010001&FLNO=310) : 有罪之判決書，應於理由內分別情形記載下列事項：
  1. 認定犯罪事實所憑之證據及其認定之理由。
  2. 對於被告有利之證據不採納者，其理由。
  3. 科刑時就刑法第五十七條或第五十八條規定事項所審酌之情形。
  4. 刑罰有加重、減輕或免除者，其理由。
  5. 易以訓誡或緩刑者，其理由。
  6. 諭知沒收、保安處分者，其理由。
  7. 適用之法律。
- 第 310-1 條 : 有罪判決，諭知六月以下有期徒刑或拘役得易科罰金、罰金或免刑者，其判決書得僅記載判決主文、犯罪事實、證據名稱、對於被告有利證據不採納之理由及應適用之法條。前項判決，法院認定之犯罪事實與起訴書之記載相同者，得引用之。
- 第 310-2 條 : 適用簡式審判程序之有罪判決書之製作，準用第四百五十四條之規定。
- 第 310-3 條 : 除於有罪判決諭知沒收之情形外，諭知沒收之判決，應記載其裁判之主文、構成沒收之事實與理由。理由內應分別情形記載認定事實所憑之證據及其認定之理由、對於被告有利證據不採納之理由及應適用之法律。
- 第 311 條 : 宣示判決，應自辯論終結之日起十四日內為之。
- 第 312 條	: 宣示判決，被告雖不在庭亦應為之。
- 第 313 條	: 宣示判決，不以參與審判之推事為限。
- 第 314 條	:判決得為上訴者，其上訴期間及提出上訴狀之法院，應於宣示時一併告知，並應記載於送達被告之判決正本。前項判決正本，並應送達於告訴人及告發人，告訴人於上訴期間內，得向檢察官陳述意見。
- 第 314-1 條 : 有罪判決之正本，應附記論罪之法條全文。


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
