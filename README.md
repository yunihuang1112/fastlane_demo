# fastlane_demo
A demo for how to setup testing with fastlane in Swift.  
This demo tests the uitest by screenshot with Fastlane.  

* ### Before starting  
Before you using this demo, install fastlane first.  
See [here](https://docs.fastlane.tools/getting-started/ios/setup/) to install fastlane.

* ### Start demo
After installed, create a project with some ui.  
In this demo, we have two page, the first page(PageOneVC) and second page(PageTwoVC).  
And having a button in PageOneVC, a label in PageTwoVC.  
Just to let you known that they are not the same page.  

* ### What we want to test?  
1. When we first enter the PageOneVC, the button will show "first_in".
2. When tapping the button, it will go to PageTwoVC.
3. Then tapping the back button on the navigatoin bar.
4. And we back to PageOneVC, the button will show "viewWillAppear".  

* ### Writing UI test  
By knowning what we want to test, we can use the XCUIApplication, XCUIElementQuery and XCTAssert to test.
1. Lanch app.
2. Check the button named "first_in" and the button named "viewWillAppear" exist or not.
3. Tap the button.
4. Check back button exists or not.
5. Tap back.   
6. Check the button named "first_in" and the button named "viewWillAppear" exist or not.  

* ### Test by fastlane snapshot  
Initialize snapshot by seeing [here](https://docs.fastlane.tools/getting-started/ios/screenshots/).  
Then run "fastlane snapshot".  

Then you will see a html created in the path: ./project/screenshots/screenshots.html.  
The html will look like this:  
  
![](https://github.com/yunihuang1112/fastlane_demo/blob/master/demo_snapshot_html.png)

* ### Test all test by fastlane   
Run "fastlane scan", and it will automatically run all the tests in the project.  
And you will see like this:  
  
![](https://github.com/yunihuang1112/fastlane_demo/blob/master/demo_test_all.png)
