## 作品集計畫
#### 程式
  * 小精靈: CSS
  * 萬年曆: PHP、CSS
  * 統一發票: PHP、CSS
  * 數位時鐘: JavaScript、CSS
  * 類比時鐘: JavaScript、CSS
  * 1/2遊戲: JavaScript、jQuery、CSS
  * 
#### 平面設計
  * 冰品DM: Photoshop
  * 年曆: Photoshop
  * logo設計: Illustrator


## 視覺計畫
  * 採簡潔的風格，主要配色為白色與綠色


## 功能規劃
1. 帳號管理
  - 使用者帳號處理
  - 可以新增、刪除、修改
  - 管理者帳號不可做變更與刪除
2. 個人基本資料管理
  - 個人基本資料處理，可以修改，但不可以新增與刪除，唯有一筆資料
  - 大頭貼的圖片利用下拉選單的方式，取用"圖片管理"中的圖片
3. 連結管理
  - 相關連結的處理，可以新增、刪除、修改，也可以選擇是否隱藏與調整排列的順序
4. 自傳管理
  - 自傳資料處理，可以新增、刪除、修改
  - 可有多筆自傳，但只會在前台顯示一筆資料
5. 求職條件管理
  - 求職條件資料處理，可以新增、刪除、修改，也可以選擇是否隱藏與調整排列的順序
6. 學經歷管理
  - 學經歷資料處理，可以新增、刪除、修改，也可以選擇是否隱藏與調整排列的順序
7. 工作技能管理
  - 工作技能資料處理，可以新增、刪除、修改，也可以選擇是否隱藏與調整排列的順序
  - 分為技能種類與技能項目兩個區塊，可以各別的做調整與修改
  - 刪除父類別不會使子類別的項目一併被刪除
8. 作品集管理
  - 作品集資料處理，可以新增、刪除、修改，也可以選擇是否隱藏與調整排列的順序
  - 作品的預覽圖片利用下拉選單的方式，取用"圖片管理"中的圖片
9.  圖片管理
  - 圖片處理，可以新增、刪除、修改
  - 處理所有圖片的上傳，其他頁面若需要圖片，可以使用下拉選單，選取該資料表的圖片來取用
10. 登入
  - 有登入的功能，若沒有登入則不可進入後台區域


## 資料庫
1. 個人基本資料表 - resume_myInfo
  - id        流水號
  - name      姓名
  - engName   英文姓名
  - phone     電話
  - email     信箱
  - birth     生日
  - city      居住縣市
  - info      簡介
  - imgId     圖片ID
2. 連結資料表 - resume_link
  - id        流水號
  - web       網頁
  - link      連結
  - icon      圖示(font awesome)
  - orderNum  排序
  - sh        顯示(1或0) 
3. 學經歷資料表 - resume_experience
  - id        流水號
  - item      項目
  - time      時間(年+月)
  - content   內容
  - type      1:工作經歷，0:學歷
  - orderNum  排序
  - sh        顯示(1或0) 
4. 自傳資料表 - resume_autobiography
  - id        流水號
  - content   內容
  - note      備註
  - sh        顯示(1或0)  擇一顯示
5. 求職條件資料表 - resume_jobCondition
  - id        流水號
  - item      項目
  - content   內容
  - orderNum  排序
  - sh        顯示(1或0) 
6. 作品集資料表 - resume_portfolio
  - id        流水號
  - item      項目
  - content   內容
  - link      連結
  - type      作品類型
  - imgId     圖片ID
  - orderNum  排序
  - sh        顯示(1或0) 
7. 圖片資料表 - resume_img
  - id        流水號
  - name      圖片備註
  - img       圖檔名
8. 工作技能資料表 - resume_skill
  - id        流水號
  - skill     技能
  - percent   百分比
  - parent    父元素
  - orderNum  排序
  - type      0:種類，1:項目
  - sh        顯示(1或0) 
9. 使用者資料表 - resume_admin
  - id        流水號
  - acc       帳號
  - pw        密碼
#### 圖片資料表記錄所有上傳的圖片，其他需要取用圖片的資料表，都會存取該表的ID值

