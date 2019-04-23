# Tutorial---Fastlane

Fastlane auto screenshot 跟 deliver

# 第一部分 - 安裝 Fastlane ( 有安裝過跳到第二步驟 )

# 第二部分 - 建立好 UITest

* 配置 Scheme

[](images/schema.png)

* 撰寫 UITest

[](images/uitest.png)

# 第三部分 - Fastlane 前置配置

* fastlane init

# 第四部分 - screenshot 前置配置

* fastlane snapshot init

* 把 ./SnapshotHelper.swift 加到 unittest 裡面

*    let app = XCUIApplication()
        setupSnapshot(app)
        app.launch()

* 修正參數檔 Snapfile

	* 選擇需要的 device

	* instruments -s devices

* Run **fastlane snapshot**

# 第五部分 - 自動更新上架資訊

fastlane deliver

# 第六部分 - Fastfile

新增

lane :screenshots do
  capture_screenshots
  upload_to_app_store
end

使用 

fastlane

# 第七部分 - 自動增加版本號

[自動增加版本號](https://developer.apple.com/library/archive/qa/qa1827/_index.html)

![](images/autoadd.png)







