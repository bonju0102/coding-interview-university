# [譯] Coding Interview University 一套完整的學習手冊幫助自己準備 Google 的面試

> * 原文地址：[Coding Interview University](https://github.com/jwasham/coding-interview-university)
* 原文作者：[John Washam](https://github.com/jwasham)
* 譯文出自：[掘金翻譯計劃](https://github.com/xitu/gold-miner)
* 譯者：[aleen42](https://github.com/aleen42)，[Newton](https://github.com/Newt0n)，[bobmayuze](https://github.com/bobmayuze)，[ Jaeger](https://github.com/laobie)，[sqrthree](https://github.com/sqrthree)

[![xitu](https://camo.githubusercontent.com/c9c9db0a39b56738a62332f0791d58b1522fdf82/68747470733a2f2f7261776769742e636f6d2f616c65656e34322f6261646765732f6d61737465722f7372632f786974752e737667)](https://github.com/xitu/gold-miner)

## 這是？

這是我為了從 web 開發者（自學、非計算機科學學位）蛻變至 Google 軟件工程師所製定的計劃，其內容歷時數月。

![白板上編程 ———— 來自 HBO 頻道的劇集，“矽谷”](https://d3j2pkmjtin6ou.cloudfront.net/coding-at-the-whiteboard-silicon-valley.png)

這一長列表是從 **Google 的指導筆記** 中萃取出來並進行擴展。因此，有些事情你必須去了解一下。我在列表的底部添加了一些額外項，用於解決面試中可能會出現的問題。這些額外項大部分是來自於Steve Yegge 的“[得到在Google 工作的機會](http://steve-yegge.blogspot.com/2008/03/get-that-job-at-google.html)” 。而在 Google 指導筆記的逐字間，它們有時也會被反映出來。

---

## 目錄

- [這是？ ](#這是)
- [為何要用到它？ ](#為何要用到它)
- [如何使用它](#如何使用它)
- [擁有一名 Googler 的心態](#擁有一名-googler-的心態)
- [我得到了工作嗎？ ](#我得到了工作嗎)
- [跟著我的腳步](#跟著我的腳步)
- [不要妄自菲薄](#不要妄自菲薄)
- [關於 Google](#關於-google)
- [相關視頻資源](#相關視頻資源)
- [面試過程 & 通用的面試準備](#面試過程--通用的面試準備)
- [為你的面試選擇一種語言](#為你的面試選擇一種語言)
- [在你開始之前](#在你開始之前)
- [你所看不到的](#你所看不到的)
- [日常計劃](#日常計劃)
- [必備知識](#必備知識)
- [算法複雜度 / Big-O / 漸進分析法](#算法複雜度--big-o--漸進分析法)
- [數據結構](#數據結構)
    - [數組（Arrays）](#數組arrays)
    - [鍊錶（Linked Lists）](#鍊錶linked-lists)
    - [堆棧（Stack）](#堆棧stack)
    - [隊列（Queue）](#隊列queue)
    - [哈希表（Hash table）](#哈希表hash-table)
- [更多的知識](#更多的知識)
    - [二分查找（Binary search）](#二分查找binary-search)
    - [按位運算（Bitwise operations）](#按位運算bitwise-operations)
- [樹（Trees）](#樹trees)
    - [樹 —— 筆記 & 背景](#樹--筆記--背景)
    - [二叉查找樹（Binary search trees）：BSTs](#二叉查找樹binary-search-treesbsts)
    - [堆（Heap） / 優先級隊列（Priority Queue） / 二叉堆（Binary Heap）](#堆heap--優先級隊列priority-queue--二叉堆binary-heap)
    - [字典樹（Tries）](#字典樹tries)
    - [平衡查找樹（Balanced search trees）](#平衡查找樹balanced-search-trees)
    - [N 叉樹（K 叉樹、M 叉樹）](#n-叉樹k-叉樹m-叉樹)
- [排序](#排序sorting)
- [圖（Graphs）](#圖graphs)
- [更多知識](#更多知識)
    - [遞歸](#遞歸recursion)
    - [動態規劃](#動態規劃dynamic-programming)
    - [組合 & 概率](#組合combinatorics-n-中選-k-個--概率probability)
    - [NP, NP-完全和近似算法](#np-np-完全和近似算法)
    - [緩存](#緩存cache)
    - [進程和線程](#進程processe和線程thread)
    - [系統設計、可伸縮性、數據處理](#系統設計可伸縮性數據處理)
    - [論文](#論文)
    - [測試](#測試)
    - [調度](#調度)
    - [實現系統例程](#實現系統例程)
    - [字符串搜索和操作](#字符串搜索和操作)
- [終面](#終面)
- [書籍](#書籍)
- [編碼練習和挑戰](#編碼練習和挑戰)
- [當你臨近面試時](#當你臨近面試時)
- [你的簡歷](#你的簡歷)
- [當面試來臨的時候](#當面試來臨的時候)
- [問面試官的問題](#問面試官的問題)
- [當你獲得了夢想的職位](#當你獲得了夢想的職位)

---------------- 下面的內容是可選的 ----------------

- [附加的學習](#附加的學習)
    - [Unicode](#unicode)
    - [字節順序](#字節順序)
    - [Emacs and vi(m)](#emacs-and-vim)
    - [Unix 命令行工具](#unix-命令行工具)
    - [信息資源 (視頻)](#信息資源-視頻)
    - [奇偶校驗位 & 漢明碼 (視頻)](#奇偶校驗位--漢明碼-視頻)
    - [系統熵值（系統複雜度）](#系統熵值系統複雜度)
    - [密碼學](#密碼學)
    - [壓縮](#壓縮)
    - [網絡 (視頻)](#網絡-視頻)
    - [計算機安全](#計算機安全)
    - [釋放緩存](#釋放緩存)
    - [並行/並發編程](#並行並發編程)
    - [設計模式](#設計模式)
    - [信息傳輸, 序列化, 和隊列化的系統](#信息傳輸-序列化和隊列化的系統)
    - [快速傅里葉變換](#快速傅里葉變換)
    - [布隆過濾器](#布隆過濾器)
    - [van Emde Boas 樹](#van-emde-boas-樹)
    - [更深入的數據結構](#更深入的數據結構)
    - [跳表](#跳表)
    - [網絡流](#網絡流)
    - [不相交集 & 聯合查找](#不相交集--聯合查找)
    - [快速處理數學](#math-for-fast-processing)
    - [樹堆 (Treap)](#樹堆-treap)
    - [線性規劃](#線性規劃linear-programming視頻)
    - [幾何：凸包（Geometry, Convex hull）](#幾何凸包geometry-convex-hull視頻)
    - [離散數學](#離散數學)
    - [機器學習](#機器學習machine-learning)
    - [Go 語言](#go-語言)
- [一些主題的額外內容](#一些主題的額外內容)
- [視頻系列](#視頻系列)
- [計算機科學課程](#計算機科學課程)

---

## 為何要用到它？

我一直都是遵循該計劃去準備 Google 的面試。自 1997 年以來，我一直從事於 web 程序的構建、服務器的構建及創業型公司的創辦。對於只有著一個經濟學學位，而不是計算機科學學位（CS degree）的我來說，在職業生涯中所取得的都非常成功。然而，我想在 Google 工作，並進入大型系統中，真正地去理解計算機系統、算法效率、數據結構性能、低級別編程語言及其工作原理。可一項都不了解的我，怎麼會被 Google 所應聘呢？

當我創建該項目時，我從一個堆棧到一個堆都不了解。那時的我，完全不了解 Big-O 、樹，或如何去遍歷一個圖。如果非要我去編寫一個排序算法的話，我只能說我所寫的肯定是很糟糕。一直以來，我所用的任何數據結構都是內建於編程語言當中。至於它們在背後是如何運作，對此我一概不清楚。此外，以前的我並不需要對內存進行管理，最多就只是在一個正在執行的進程拋出了“內存不足”的錯誤後，採取一些權變措施。而在我的編程生活中，也甚少使用到多維數組，可關聯數組卻成千上萬。而且，從一開始到現在，我都還未曾自己實現過數據結構。

就是這樣的我，在經過該學習計劃後，已然對被 Google 所僱傭充滿信心。這是一個漫長的計劃，以至於花費了我數月的時間。若您早已熟悉大部分的知識，那麼也許能節省大量的時間。

## 如何使用它

下面所有的東西都只是一個概述。因此，你需要由上而下逐一地去處理它。

在學習過程中，我是使用 GitHub 特殊的語法特性 markdown flavor 去檢查計劃的進展，包括使用任務列表。

- [x] 創建一個新的分支，以使得你可以像這樣去檢查計劃的進展。直接往方括號中填寫一個字符 x 即可：[x]

[更多關於 Github-flavored markdown 的詳情](https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown)

## 我得到了工作嗎？

我還沒去應聘。

因為我離完成學習（完成該瘋狂的計劃列表）還需要數天的時間，並打算在下週開始用一整天的時間，以編程的方式去解決問題。當然，這將會持續數週的時間。然後，我才通過使用在二月份所得到的一個介紹資格，去正式應聘 Google（沒錯，是二月份時就得到的）。

    感謝 JP 的這次介紹。

## 跟著我的腳步

目前我仍在該計劃的執行過程中，如果你想跟隨我腳步去學習的話，可以登進我在 [GoogleyAsHeck.com](https://googleyasheck.com/) 上所寫的博客。

下面是我的聯繫方式：

- Twitter: [@googleyasheck](https://twitter.com/googleyasheck)
- Twitter: [@StartupNextDoor](https://twitter.com/StartupNextDoor)
- Google+: [+Googleyasheck](https://plus.google.com/+Googleyasheck)
- LinkedIn: [johnawasham](https://www.linkedin.com/in/johnawasham)

![John Washam - Coding Interview University](https://dng5l3qzreal6.cloudfront.net/2016/Aug/book_stack_photo_resized_18_1469302751157-1472661280368.png)

## 不要妄自菲薄

- Google 的工程師都是才智過人的。但是，就算是工作在 Google 的他們，仍然會因為覺得自己不夠聰明而感到一種不安。
- [天才程序員的神話](https://www.youtube.com/watch?v=0SARbwvhupQ)

## 關於 Google

- [ ] 面向學生 —— [Google 的職業生涯：技術開髮指導](https://www.google.com/about/careers/students/guide-to-technical-development.html)
- [ ] Google 檢索的原理：
    - [ ] [Google 檢索的發展史（視頻）](https://www.youtube.com/watch?v=mTBShTwCnD4)
    - [ ] [Google 檢索的原理 —— 故事篇](https://www.google.com/insidesearch/howsearchworks/thestory/)
    - [ ] [Google 檢索的原理](https://www.google.com/insidesearch/howsearchworks/)
    - [ ] [Google 檢索的原理 —— Matt Cutts（視頻）](https://www.youtube.com/watch?v=BNHR6IQJGZs)
    - [ ] [Google 是如何改善其檢索算法（視頻）](https://www.youtube.com/watch?v=J5RZOU6vK4Q)
- [ ] 系列文章：
    - [ ] [Google 檢索是如何處理移動設備](https://backchannel.com/how-google-search-dealt-with-mobile-33bc09852dc9)
    - [ ] [Google 為了尋找大眾需求的秘密研究](https://backchannel.com/googles-secret-study-to-find-out-our-needs-eba8700263bf)
    - [ ] [Google 檢索將成為你的下一個大腦](https://backchannel.com/google-search-will-be-your-next-brain-5207c26e4523)
    - [ ] [Demis Hassabis 的心靈直白](https://backchannel.com/the-deep-mind-of-demis-hassabis-156112890d8a)
- [ ] [書籍：Google 公司是如何運作的](https://www.amazon.com/How-Google-Works-Eric-Schmidt/dp/1455582344)
- [ ] [由 Google 通告所製作 —— 2016年10月（視頻）](https://www.youtube.com/watch?v=q4y0KOeXViI)

## 相關視頻資源

部分視頻只能通過在 Coursera、Edx 或 Lynda.com class 上註冊登錄才能觀看。這些視頻被稱為網絡公開課程（MOOC）。即便是免費觀看，部分課程可能會由於不在時間段內而無法獲取。因此，你需要多等待幾個月。

    很感謝您能幫我把網絡公開課程的視頻鏈接轉換成公開的視頻源，以代替那些在線課程的視頻。此外，一些大學的講座視頻也是我所青睞的。

## 面試過程 & 通用的面試準備

- [ ] 視頻：
    - [ ] [如何在 Google 工作 —— 考生指導課程（視頻）](https://www.youtube.com/watch?v=oWbUtlUhwa8&feature=youtu.be)
    - [ ] [Google 招聘者所分享的技術面試小竅門（視頻）](https://www.youtube.com/watch?v=qc1ow​​f2-220&feature=youtu.be)
    - [ ] [如何在 Google 工作：技術型簡歷的準備（視頻）](https://www.youtube.com/watch?v=8npJLXkcmu8)

- [ ] 文章：
    - [ ] [三步成為 Googler](http://www.google.com/about/careers/lifeatgoogle/hiringprocess/)
    - [ ] [得到在 Google 的工作機會](http://steve-yegge.blogspot.com/2008/03/get-that-job-at-google.html)
        - 所有他所提及的事情都列在了下面
    - [ ] _（早已過期）_ [如何得到Google 的一份工作，面試題，應聘過程](http://dondodge.typepad.com/the_next_big_thing/2010/09/how-to-get-a-job -at-google-interview-questions-hiring-process.html)
    - [ ] [電話面試的問題](http://sites.google.com/site/steveyegge2/five-essential-phone-screen-questions)

- [ ] 附加的（雖然 Google 不建議，但我還是添加在此）：
    - [ ] [ABC：永遠都要去編程（Always Be Coding）](https://medium.com/always-be-coding/abc-always-be-coding-d5f8051afce2#.4heg8zvm4)
    - [ ] [四步成為 Google 裡一名沒有學位的員工](https://medium.com/always-be-coding/four-steps-to-google-without-a-degree-8f381aa6bd5e#.asalo1vfx)
    - [ ] [共享白板（Whiteboarding）](https://medium.com/@dpup/whiteboarding-4df873dbba2e#.hf6jn45g1)
    - [ ] [Google 是如何看待應聘、管理和公司文化](http://www.kpcb.com/blog/lessons-learned-how-google-thinks-about-hiring-management-and-culture)
    - [ ] [程序開發麵試中有效的白板（Whiteboarding）](http://www.coderust.com/blog/2014/04/10/effective-whiteboarding-during-programming-interviews/)
    - [ ] 震撼開發類面試 第一集：
        - [ ] [Gayle L McDowell —— 震撼開發類面試（視頻）](https://www.youtube.com/watch?v=rEJzOhC5ZtQ)
        - [ ] [震撼開發類面試 —— 作者 Gayle Laakmann McDowell（視頻）](https://www.youtube.com/watch?v=aClxtDcdpsQ)
    - [ ] 如何在世界四強企業中獲得一份工作：
        - [ ] [“如何在世界四強企業中獲得一份工作 —— Amazon、Facebook、Google 和 Microsoft”（視頻）](https://www.youtube.com/watch?v=YJZCUhxNCv8)
    - [ ] [面試 Google 失敗](http://alexbowe.com/failing-at-google-interviews/)

## 為你的面試選擇一種語言

在這，我就以下話題寫一篇短文—— [重點：為在Google 的面試選擇一種語言](https://googleyasheck.com/important-pick-one-language-for-the-google-interview /)

在大多數公司的面試當中，你可以在編程這一環節，使用一種自己用起來較為舒適的語言去完成編程。但在 Google，你只有三種固定的選擇：

- C++
- Java
- Python

有時你也可以使用下面兩種，但需要事先查閱說明。因為，說明中會有警告：

- JavaScript
- Ruby

你需要對你所選擇的語言感到非常舒適且足夠了解。

更多關於語言選擇的閱讀：

- http://www.byte-by-byte.com/choose-the-right-language-for-your-coding-interview/
- http://blog.codingforinterviews.com/best-programming-language-jobs/
- https://www.quora.com/What-is-the-best-language-to-program-in-for-an-in-person-Google-interview

[在此查看相關語言的資源](../programming-language-resources.md)

由於，我正在學習C、C++ 和 Python。因此，在下面你會看到部分關於它們的學習資料。相關書籍請看文章的底部。

## 在你開始之前

該列表已經持續更新了很長的一段時間，所以，我們的確很容易會對其失去控制。

這裡列出了一些我所犯過的錯誤，希望您不要重滔覆轍。

### 1. 你不可能把所有的東西都記住

就算我查看了數小時的視頻，並記錄了大量的筆記。幾個月後的我，仍然會忘卻其中大部分的東西。所以，我翻閱了我的筆記，並將可回顧的東西製作成抽認卡（flashcard）（請往下看）

### 2. 使用抽認卡

為了解決善忘的問題，我製作了一些關於抽認卡的頁面，用於添加兩種抽認卡：正常的及帶有代碼的。每種卡都會有不同的格式設計。

而且，我還以移動設備為先去設計這些網頁，以使得在任何地方的我，都能通過我的手機及平板去回顧知識。

你也可以免費製作屬於你自己的抽認卡網站：

- [抽認卡頁面的代碼倉庫](https://github.com/jwasham/computer-science-flash-cards)
- [我的抽認卡數據庫](https://github.com/jwasham/computer-science-flash-cards/blob/master/cards-jwasham.db)：有一點需要記住的是，我做事有點過頭，以至於把卡片都覆蓋到所有的東西上。從彙編語言和 Python 的細枝末節，乃至到機器學習和統計都被覆蓋到卡片上。而這種做法，對於 Google 的要求來說，卻是多餘。

**在抽認卡上做筆記：** 若你第一次發現你知道問題的答案時，先不要急著把其標註成“已懂”。你需要做的，是去查看一下是否有同樣的抽認卡，並在你真正懂得如何解決問題之前，多問自己幾次。重複地問答可幫助您深刻記住該知識點。

### 3. 回顧，回顧，回顧

我留有一組 ASCII 碼表、OSI 堆棧、Big-O 記號及更多的小抄紙，以便在空餘的時候可以學習。

每編程半個小時就要休息一下，並去回顧你的抽認卡。

### 4. 專注

在學習的過程中，往往會有許多令人分心的事佔據著我們寶貴的時間。因此，專注和集中註意力是非常困難的。

## 你所看不到的

由於，這個巨大的列表一開始是作為我個人從 Google 面試指導筆記所形成的一個事件處理列表。因此，有一些我熟悉且普遍的技術在此都未被談及到：

- SQL
- Javascript
- HTML、CSS 和其他前端技術

## 日常計劃

部分問題可能會花費一天的時間去學習，而部分則會花費多天。當然，有些學習並不需要我們懂得如何實現。

因此，每一天我都會在下面所列出的列表中選擇一項，並查看相關的視頻。然後，使用以下的一種語言去實現：

    C —— 使用結構體和函數，該函數會接受一個結構體指針 * 及其他數據作為參數。
    C++ —— 不使用內建的數據類型。
    C++ —— 使用內建的數據類型，如使用 STL 的 std::list 來作為鍊錶。
    Python —— 使用內建的數據類型（為了持續練習 Python），並編寫一些測試去保證自己代碼的正確性。有時，只需要使用斷言函數 assert() 即可。
    此外，你也可以使用 Java 或其他語言。以上只是我的個人偏好而已。

為何要在這些語言上分別實現一次？

    因為可以練習，練習，練習，直至我厭倦它，並完美地實現出來。 （若有部分邊緣條件沒想到時，我會用書寫的形式記錄下來並去記憶）
    因為可以在純原生的條件下工作（不需垃圾回收機制的幫助下，分配/釋放內存（除了 Python））
    因為可以利用上內建的數據類型，以使得我擁有在現實中使用內建工具的經驗（在生產環境中，我不會去實現自己的鍊錶）

就算我沒有時間去每一項都這麼做，但我也會盡我所能的。

在這裡，你可以查看到我的代碼：
 - [C](https://github.com/jwasham/practice-c)
 - [C++](https://github.com/jwasham/practice-cpp)
 - [Python](https://github.com/jwasham/practice-python)

你不需要記住每一個算法的內部原理。

在一個白板上寫代碼，而不要直接在計算機上編寫。在測試完部分簡單的輸入後，到計算機上再測試一遍。

## 必備知識

- [ ] **計算機是如何處理一段程序：**
    - [ ] [CPU 是如何執行代碼（視頻）](https://www.youtube.com/watch?v=42KTvGYQYnA)
    - [ ] [機器碼指令（視頻）](https://www.youtube.com/watch?v=Mv2XQgpbTNE)

- [ ] **編譯器**
    - [ ] [編譯器是如何在 ~1 分鐘內工作（視頻）](https://www.youtube.com/watch?v=IhC7sdYe-Jg)
    - [ ] [Hardvard CS50 —— 編譯器（視頻）](https://www.youtube.com/watch?v=CSZLNYF4Klo)
    - [ ] [C++（視頻）](https://www.youtube.com/watch?v=twodd1KFfGk)
    - [ ] [掌握編譯器的優化（C++）（視頻）](https://www.youtube.com/watch?v=FnGCDLhaxKU)

- [ ] **浮點數是如何存儲的：**
    - [ ] 簡單的8-bit：[浮點數的表達形式—— 1（視頻—— 在計算上有一個錯誤—— 詳情請查看視頻的介紹）](https://www.youtube.com/watch ?v=ji3SfClm8TU)
    - [ ] 32 bit：[IEEE754 32-bit 浮點二進制（視頻）](https://www.youtube.com/watch?v=50ZYcZebIec)

## 算法複雜度 / Big-O / 漸進分析法
- 並不需要實現
- [ ] [Harvard CS50 —— 漸進表示（視頻）](https://www.youtube.com/watch?v=iOq5kSKqeR4)
- [ ] [Big O 記號（通用快速教程）（視頻）](https://www.youtube.com/watch?v=V6mKVRU1evU)
- [ ] [Big O 記號（以及 Omega 和 Theta）—— 最佳數學解釋（視頻）](https://www.youtube.com/watch?v=ei-A_wy5Yxw&index=2&list=PL1BaGV1cIH4UhkL8a9bJGG356covJ76qN)
- [ ] Skiena 算法：
    - [視頻](https://www.youtube.com/watch?v=gSyDMtdPNpU&index=2&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [幻燈片](http://www3.cs.stonybrook.edu/~algorith/video-lectures/2007/lecture2.pdf)
- [ ] [對於算法複雜度分析的一次詳細介紹](http://discrete.gr/complexity/)
- [ ] [增長階數（Orders of Growth）（視頻）](https://class.coursera.org/algorithmicthink1-004/lecture/59)
- [ ] [漸進性（Asymptotics）（視頻）](https://class.coursera.org/algorithmicthink1-004/lecture/61)
- [ ] [UC Berkeley Big O（視頻）](https://youtu.be/VIS4YDpuP98)
- [ ] [UC Berkeley Big Omega（視頻）](https://youtu.be/ca3e7UVmeUc)
- [ ] [平攤分析法（Amortized Analysis）（視頻）](https://www.youtube.com/watch?v=B3SpQZaAZP4&index=10&list=PL1BaGV1cIH4UhkL8a9bJGG356covJ76qN)
- [ ] [舉證“Big O”（視頻）](https://class.coursera.org/algorithmicthink1-004/lecture/63)
- [ ] 高級編程（包括遞歸關係和主定理）：
    - [計算性複雜度：第一部](https://www.topcoder.com/community/data-science/data-science-tutorials/computational-complexity-section-1/)
    - [計算性複雜度：第二部](https://www.topcoder.com/community/data-science/data-science-tutorials/computational-complexity-section-2/)
- [ ] [速查表（Cheat sheet）](http://bigocheatsheet.com/)

    如果部分課程過於學術性，你可直接跳到文章底部，去查看離散數學的視頻以獲取相關背景知識。

## 數據結構

- ### 數組（Arrays）
    - 實現一個可自動調整大小的動態數組。
    - [ ] 介紹：
        - [數組（視頻）](https://www.coursera.org/learn/data-structures/lecture/OsBSF/arrays)
        - [數組的基礎知識（視頻）](https://archive.org/details/0102WhatYouShouldKnow/02_04-basicArrays.mp4)
        - [多維數組（視頻）](https://archive.org/details/0102WhatYouShouldKnow/02_05-multidimensionalArrays.mp4)
        - [動態數組（視頻）](https://www.coursera.org/learn/data-structures/lecture/EwbnV/dynamic-arrays)
        - [不規則數組（視頻）](https://archive.org/details/0102WhatYouShouldKnow/02_06-jaggedArrays.mp4)
        - [調整數組的大小（視頻）](https://archive.org/details/0102WhatYouShouldKnow/03_01-resizableArrays.mp4)
    - [ ] 實現一個動態數組（可自動調整大小的可變數組）：
        - [ ] 練習使用數組和指針去編碼，並且指針是通過計算去跳轉而不是使用索引
        - [ ] 通過分配內存來新建一個原生數據型數組
            - 可以使用 int 類型的數組，但不能使用其語法特性
            - 從大小為16或更大的數（使用2的倍數 —— 16、32、64、128）開始編寫
        - [ ] size() —— 數組元素的個數
        - [ ] capacity() —— 可容納元素的個數
        - [ ] is_empty()
        - [ ] at(index) —— 返回對應索引的元素，且若索引越界則憤然報錯
        - [ ] push(item)
        - [ ] insert(index, item) —— 在指定索引中插入元素，並把後面的元素依次後移
        - [ ] prepend(item) —— 可以使用上面的 insert 函數，傳參 index 為 0
        - [ ] pop() —— 刪除在數組末端的元素，並返回其值
        - [ ] delete(index) —— 刪除指定索引的元素，並把後面的元素依次前移
        - [ ] remove(item) —— 刪除指定值的元素，並返回其索引（即使有多個元素）
        - [ ] find(item) —— 尋找指定值的元素並返回其中第一個出現的元素其索引，若未找到則返回 -1
        - [ ] resize(new_capacity) // 私有函數
            - 若數組的大小到達其容積，則變大一倍
            - 獲取元素後，若數組大小為其容積的1/4，則縮小一半
    - [ ] 時間複雜度
        - 在數組末端增加/刪除、定位、更新元素，只允許佔 O(1) 的時間複雜度（平攤（amortized）去分配內存以獲取更多空間）
        - 在數組任何地方插入/移除元素，只允許 O(n) 的時間複雜度
    - [ ] 空間複雜度
        - 因為在內存中分配的空間鄰近，所以有助於提高性能
        - 空間需求 = （大於或等於 n 的數組容積）* 元素的大小。即便空間需求為 2n，其空間複雜度仍然是 O(n)

- ### 鍊錶（Linked Lists）
    - [ ] 介紹：
        - [ ] [單向鍊錶（視頻）](https://www.coursera.org/learn/data-structures/lecture/kHhgK/singly-linked-lists)
        - [ ] [CS 61B —— 鍊錶（視頻）](https://www.youtube.com/watch?v=sJtJOtXCW_M&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=5)
    - [ ] [C 代碼（視頻）](https://www.youtube.com/watch?v=QN6FPiD0Gzo)
        - 並非看完整個視頻，只需要看關於節點結果和內存分配那一部分即可
    - [ ] 鍊錶 vs 數組：
        - [基本鍊錶 Vs 數組（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/rjBs9/core-linked-lists-vs-arrays)
        - [在現實中，鍊錶Vs 數組（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/QUaUd/in-the-real-world-lists-vs- arrays)
    - [ ] [為什麼你需要避免使用鍊錶（視頻）](https://www.youtube.com/watch?v=YQs6IC-vgmo)
    - [ ] 的確：你需要關於“指向指針的指針”的相關知識：（因為當你傳遞一個指針到一個函數時，該函數可能會改變指針所指向的地址）該頁只是為了讓你了解“指向指針的指針”這一概念。但我並不推薦這種鍊式遍歷的風格。因為，這種風格的代碼，其可讀性和可維護性太低。
        - [指向指針的指針](https://www.eskimo.com/~scs/cclass/int/sx8.html)
    - [ ] 實現（我實現了使用尾指針以及沒有使用尾指針這兩種情況）：
        - [ ] size() —— 返回鍊錶中數據元素的個數
        - [ ] empty() —— 若鍊錶為空則返回一個布爾值 true
        - [ ] value_at(index) —— 返回第 n 個元素的值（從0開始計算）
        - [ ] push_front(value) —— 添加元素到鍊錶的首部
        - [ ] pop_front() —— 刪除首部元素並返回其值
        - [ ] push_back(value) —— 添加元素到鍊錶的尾部
        - [ ] pop_back() —— 刪除尾部元素並返回其值
        - [ ] front() —— 返回首部元素的值
        - [ ] back() —— 返回尾部元素的值
        - [ ] insert(index, value) —— 插入值到指定的索引，並把當前索引的元素指向到新的元素
        - [ ] erase(index) —— 刪除指定索引的節點
        - [ ] value_n_from_end(n) —— 返回倒數第 n 個節點的值
        - [ ] reverse() —— 逆序鍊錶
        - [ ] remove_value(value) —— 刪除鍊錶中指定值的第一個元素
    - [ ] 雙向鍊錶
        - [介紹（視頻）](https://www.coursera.org/learn/data-structures/lecture/jpGKD/doubly-linked-lists)
        - 並不需要實現

- ### 堆棧（Stack）
    - [ ] [堆棧（視頻）](https://www.coursera.org/learn/data-structures/lecture/UdKzQ/stacks)
    - [ ] [使用堆棧 —— 後進先出（視頻）](https://archive.org/details/0102WhatYouShouldKnow/05_01-usingStacksForLast-inFirst-out.mp4)
    - [ ] 可以不實現，因為使用數組來實現並不重要

- ### 隊列（Queue）
    - [ ] [使用隊列 —— 先進先出（視頻）](https://archive.org/details/0102WhatYouShouldKnow/05_03-usingQueuesForFirst-inFirst-out.mp4)
    - [ ] [隊列（視頻）](https://www.coursera.org/learn/data-structures/lecture/EShpq/queue)
    - [ ] [原型隊列/先進先出（FIFO）](https://en.wikipedia.org/wiki/Circular_buffer)
    - [ ] [優先級隊列（視頻）](https://archive.org/details/0102WhatYouShouldKnow/05_04-priorityQueuesAndDeques.mp4)
    - [ ] 使用含有尾部指針的鍊錶來實現:
        - enqueue(value) —— 在尾部添加值
        - dequeue() —— 刪除最早添加的元素並返回其值（首部元素）
        - empty()
    - [ ] 使用固定大小的數組實現：
        - enqueue(value) —— 在可容的情況下添加元素到尾部
        - dequeue() —— 刪除最早添加的元素並返回其值
        - empty()
        - full()
    - [ ] 花銷：
        - 在糟糕的實現情況下，使用鍊錶所實現的隊列，其入列和出列的時間複雜度將會是 O(n)。因為，你需要找到下一個元素，以致循環整個隊列
        - enqueue：O(1)（平攤（amortized）、鍊錶和數組 [探測（probing）]）
        - dequeue：O(1)（鍊錶和數組）
        - empty：O(1)（鍊錶和數組）

- ### 哈希表（Hash table）
    - [ ] 視頻：
        - [ ] [鍊式哈希表（視頻）](https://www.youtube.com/watch?v=0M_kIqhwbFo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=8)
        - [ ] [Table Doubling 和 Karp-Rabin（視頻）](https://www.youtube.com/watch?v=BRO7mVIFt08&index=9&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
        - [ ] [Open Addressing 和密碼型哈希（Cryptographic Hashing）（視頻）](https://www.youtube.com/watch?v=rvdJDijO2Ro&index=10&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
        - [ ] [PyCon 2010：The Mighty Dictionary（視頻）](https://www.youtube.com/watch?v=C4Kc8xzcA68)
        - [ ] [（進階）隨機取樣（Randomization）：全域哈希（Universal Hashing）& 完美哈希（Perfect Hashing）（視頻）](https://www.youtube.com/watch?v=z0lJ2k0sl1g&list= PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=11)
        - [ ] [（進階）完美哈希（Perfect hashing）（視頻）](https://www.youtube.com/watch?v=N0COwN14gt0&list=PL2B4EEwhKD-NbwZ4ezj7gyc_3yNrojKM9&index=4)

    - [ ] 在線課程：
        - [ ] [哈希函數的掌握（視頻）](https://archive.org/details/0102WhatYouShouldKnow/06_02-understandingHashFunctions.mp4)
        - [ ] [使用哈希表（視頻）](https://archive.org/details/0102WhatYouShouldKnow/06_03-usingHashTables.mp4)
        - [ ] [哈希表的支持（視頻）](https://archive.org/details/0102WhatYouShouldKnow/06_04-supportingHashing.mp4)
        - [ ] [哈希表的語言支持（視頻）](https://archive.org/details/0102WhatYouShouldKnow/06_05-languageSupportForHashTables.mp4)
        - [ ] [基本哈希表（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/m7UuP/core-hash-tables)
        - [ ] [數據結構（視頻）](https://www.coursera.org/learn/data-structures/home/week/3)
        - [ ] [電話薄問題（Phone Book Problem）（視頻）](https://www.coursera.org/learn/data-structures/lecture/NYZZP/phone-book-problem)
        - [ ] 分佈式哈希表：
            - [Dropbox 中的瞬時上傳及存儲優化（視頻）](https://www.coursera.org/learn/data-structures/lecture/DvaIb/instant-uploads-and-storage-optimization-in-dropbox)
            - [分佈式哈希表（視頻）](https://www.coursera.org/learn/data-structures/lecture/tvH8H/distributed-hash-tables)

    - [ ] 使用線性探測的數組去實現
        - hash(k, m) —— m 是哈希表的大小
        - add(key, value) —— 如果 key 已存在則更新值
        - exists(key)
        - get(key)
        - remove(key)

## 更多的知識

- ### 二分查找（Binary search）
    - [ ] [二分查找（視頻）](https://www.youtube.com/watch?v=D5SrAga1pno)
    - [ ] [二分查找（視頻）](https://www.khanacademy.org/computing/computer-science/algorithms/binary-search/a/binary-search)
    - [ ] [詳情](https://www.topcoder.com/community/data-science/data-science-tutorials/binary-search/)
    - [ ] 實現：
        - 二分查找（在一個已排序好的整型數組中查找）
        - 迭代式二分查找

- ### 按位運算（Bitwise operations）
    - [ ] [Bits 速查表](https://github.com/jwasham/coding-interview-university/blob/master/extras/cheat%20sheets/bits-cheat-sheet.pdf)
        - 你需要知道大量2的冪數值（從2^1 到 2^16 及 2^32）
    - [ ] 好好理解位操作符的含義：&、|、^、~、>>、<<
        - [ ] [字碼（words）](https://en.wikipedia.org/wiki/Word_(computer_architecture))
        - [ ] 好的介紹：
            [位操作（視頻）](https://www.youtube.com/watch?v=7jkIUgLC29I)
        - [ ] [C 語言編程教程 2-10：按位運算（視頻）](https://www.youtube.com/watch?v=d0AwjSpNXR0)
        - [ ] [位操作](https://en.wikipedia.org/wiki/Bit_manipulation)
        - [ ] [按位運算](https://en.wikipedia.org/wiki/Bitwise_operation)
        - [ ] [Bithacks](https://graphics.stanford.edu/~seander/bithacks.html)
        - [ ] [位元撫弄者（The Bit Twiddler）](http://bits.stephan-brumme.com/)
        - [ ] [交互式位元撫弄者（The Bit Twiddler Interactive）](http://bits.stephan-brumme.com/interactive.html)
    - [ ] 一補數和補碼
        - [二進制：利 & 弊（為什麼我們要使用補碼）（視頻）](https://www.youtube.com/watch?v=lKTsv6iVxV4)
        - [一補數（1s Complement）](https://en.wikipedia.org/wiki/Ones%27_complement)
        - [補碼（2s Complement）](https://en.wikipedia.org/wiki/Two%27s_complement)
    - [ ] 計算置位（Set Bits）
        - [計算一個字節中置位（Set Bits）的四種方式（視頻）](https://youtu.be/Hzuzo9NJrlc)
        - [計算比特位](https://graphics.stanford.edu/~seander/bithacks.html#CountBitsSetKernighan)
        - [如何在一個32 位的整型中計算置位（Set Bits）的數量](http://stackoverflow.com/questions/109023/how-to-count-the-number-of-set-bits- in-a-32-bit-integer)
    - [ ] 四捨五入2的冪數：
        - [四捨五入到2的下一冪數](http://bits.stephan-brumme.com/roundUpToNextPowerOfTwo.html)
    - [ ] 交換值：
        - [交換（Swap）](http://bits.stephan-brumme.com/swap.html)
    - [ ] 絕對值：
        - [絕對整型（Absolute Integer）](http://bits.stephan-brumme.com/absInteger.html)

## 樹（Trees）

- ### 樹 —— 筆記 & 背景
    - [ ] [系列：基本樹（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/ovovP/core-trees)
    - [ ] [系列：樹（視頻）](https://www.coursera.org/learn/data-structures/lecture/95qda/trees)
    - 基本的樹形結構
    - 遍歷
    - 操作算法
    - BFS（廣度優先檢索，breadth-first search）
        - [MIT（視頻）](https://www.youtube.com/watch?v=s-CYnVz-uh4&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=13)
        - 層序遍歷（使用隊列的 BFS 算法）
            - 時間複雜度： O(n)
            - 空間複雜度：
                - 最好情況： O(1)
                - 最壞情況：O(n/2)=O(n)
    - DFS（深度優先檢索，depth-first search）
        - [MIT（視頻）](https://www.youtube.com/watch?v=AfSk24UTFS8&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=14)
        - 筆記：
            - 時間複雜度：O(n)
            - 空間複雜度：
                - 最好情況：O(log n) - 樹的平均高度
                - 最壞情況：O(n)
        - 中序遍歷（DFS：左、節點本身、右）
        - 後序遍歷（DFS：左、右、節點本身）
        - 先序遍歷（DFS：節點本身、左、右）

- ### 二叉查找樹（Binary search trees）：BSTs
    - [ ] [二叉查找樹概覽（視頻）](https://www.youtube.com/watch?v=x6At0nzX92o&index=1&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
    - [ ] [系列（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/p82sw/core-introduction-to-binary-search-trees)
        - 從符號表開始到 BST 程序
    - [ ] [介紹（視頻）](https://www.coursera.org/learn/data-structures/lecture/E7cXP/introduction)
    - [ ] [MIT（視頻）](https://www.youtube.com/watch?v=9Jry5-82I68)
    - C/C++:
        - [ ] [二叉查找樹 —— 在 C/C++ 中實現（視頻）](https://www.youtube.com/watch?v=COZK7NATh4k&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=28)
        - [ ] [BST 的實現 —— 在堆棧和堆中的內存分配（視頻）](https://www.youtube.com/watch?v=hWokyBoo0aI&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=29)
        - [ ] [在二叉查找樹中找到最小和最大的元素（視頻）](https://www.youtube.com/watch?v=Ut90klNN264&index=30&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [尋找二叉樹的高度（視頻）](https://www.youtube.com/watch?v=_pnqMz5nrRs&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=31)
        - [ ] [二叉樹的遍歷 —— 廣度優先和深度優先策略（視頻）](https://www.youtube.com/watch?v=9RHO6jU--GU&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=32)
        - [ ] [二叉樹：層序遍歷（視頻）](https://www.youtube.com/watch?v=86g8jAQug04&index=33&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [二叉樹的遍歷：先序、中序、後序（視頻）](https://www.youtube.com/watch?v=gm8DUJJhmY4&index=34&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [判斷一棵二叉樹是否為二叉查找樹（視頻）](https://www.youtube.com/watch?v=yEwSGhSsT0U&index=35&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [從二叉查找樹中刪除一個節點（視頻）](https://www.youtube.com/watch?v=gcULXE7ViZw&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=36)
        - [ ] [二叉查找樹中序遍歷的後繼者（視頻）](https://www.youtube.com/watch?v=5cPbNCrdotA&index=37&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
    - [ ] 實現：
        - [ ] insert // 往樹上插值
        - [ ] get_node_count // 查找樹上的節點數
        - [ ] print_values // 從小到大打印樹中節點的值
        - [ ] delete_tree
        - [ ] is_in_tree // 如果值存在於樹中則返回 true
        - [ ] get_height // 返回節點所在的高度（如果只有一個節點，那麼高度則為1）
        - [ ] get_min // 返回樹上的最小值
        - [ ] get_max // 返回樹上的最大值
        - [ ] is_binary_search_tree
        - [ ] delete_value
        - [ ] get_successor // 返回給定值的後繼者，若沒有則返回-1

- ### 堆（Heap） / 優先級隊列（Priority Queue） / 二叉堆（Binary Heap）
    - 可視化是一棵樹，但通常是以線性的形式存儲（數組、鍊錶）
    - [ ] [堆](https://en.wikipedia.org/wiki/Heap_(data_structure))
    - [ ] [介紹（視頻）](https://www.coursera.org/learn/data-structures/lecture/2OpTs/introduction)
    - [ ] [無知的實現（視頻）](https://www.coursera.org/learn/data-structures/lecture/z3l9N/naive-implementations)
    - [ ] [二叉樹（視頻）](https://www.coursera.org/learn/data-structures/lecture/GRV2q/binary-trees)
    - [ ] [關於樹高的討論（視頻）](https://www.coursera.org/learn/data-structures/supplement/S5xxz/tree-height-remark)
    - [ ] [基本操作（視頻）](https://www.coursera.org/learn/data-structures/lecture/0g1dl/basic-operations)
    - [ ] [完全二叉樹（視頻）](https://www.coursera.org/learn/data-structures/lecture/gl5Ni/complete-binary-trees)
    - [ ] [偽代碼（視頻）](https://www.coursera.org/learn/data-structures/lecture/HxQo9/pseudocode)
    - [ ] [堆排序 —— 跳到起點（視頻）](https://youtu.be/odNJmw5TOEE?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3291)
    - [ ] [堆排序（視頻）](https://www.coursera.org/learn/data-structures/lecture/hSzMO/heap-sort)
    - [ ] [構建一個堆（視頻）](https://www.coursera.org/learn/data-structures/lecture/dwrOS/building-a-heap)
    - [ ] [MIT：堆與堆排序（視頻）](https://www.youtube.com/watch?v=B7hVxCmfPtM&index=4&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [CS 61B Lecture 24：優先級隊列（視頻）](https://www.youtube.com/watch?v=yIUFT6AKBGE&index=24&list=PL4BBB74C7D2A1049C)
    - [ ] [構建線性時間複雜度的堆（大頂堆）](https://www.youtube.com/watch?v=MiyLo8adrWw)
    - [ ] 實現一個大頂堆：
        - [ ] insert
        - [ ] sift_up —— 用於插入元素
        - [ ] get_max —— 返回最大值但不移除元素
        - [ ] get_size() —— 返回存儲的元素數量
        - [ ] is_empty() —— 若堆為空則返回 true
        - [ ] extract_max —— 返回最大值並移除
        - [ ] sift_down —— 用於獲取最大值元素
        - [ ] remove(i) —— 刪除指定索引的元素
        - [ ] heapify —— 構建堆，用於堆排序
        - [ ] heap_sort() —— 拿到一個未排序的數組，然後使用大頂堆進行就地排序
            - 注意：若用小頂堆可節省操作，但導致空間複雜度加倍。 （無法做到就地）

- ### 字典樹（Tries）
    - 需要注意的是，字典樹各式各樣。有些有前綴，而有些則沒有。有些使用字符串而不使用比特位來追踪路徑。
    - 閱讀代碼，但不實現。
    - [ ] [數據結構筆記及編程技術](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Tries)
    - [ ] 短課程視頻：
        - [ ] [對字典樹的介紹（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/08Xyf/core-introduction-to-tries)
        - [ ] [字典樹的性能（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/PvlZW/core-performance-of-tries)
        - [ ] [實現一棵字典樹（視頻）](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/DFvd3/core-implementing-a-trie)
    - [ ] [字典樹：一個被忽略的數據結構](https://www.toptal.com/java/the-trie-a-neglected-data-structure)
    - [ ] [高級編程 —— 使用字典樹](https://www.topcoder.com/community/data-science/data-science-tutorials/using-tries/)
    - [ ] [標準教程（現實中的用例）（視頻）](https://www.youtube.com/watch?v=TJ8SkcUSdbU)
    - [ ] [MIT，高階數據結構，使用字符串追踪路徑（可事半功倍）](https://www.youtube.com/watch?v=NinWEPPrkDQ&index=16&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)

- ### 平衡查找樹（Balanced search trees）
    - 掌握至少一種平衡查找樹（並懂得如何實現）：
    - “在各種平衡查找樹當中，AVL 樹和2-3樹已經成為了過去，而紅黑樹（red-black trees）看似變得越來越受人青睞。這種令人特別感興趣的數據結構，亦稱伸展樹（splay tree）。它可以自我管理，且會使用輪換來移除任何訪問過根節點的key。” —— Skiena
    - 因此，在各種各樣的平衡查找樹當中，我選擇了伸展樹來實現。雖然，通過我的閱讀，我發現在 Google 的面試中並不會被要求實現一棵平衡查找樹。但是，為了勝人一籌，我們還是應該看看如何去實現。在閱讀了大量關於紅黑樹的代碼後，我才發現伸展樹的實現確實會使得各方面更為高效。
        - 伸展樹：插入、查找、刪除函數的實現，而如果你最終實現了紅黑樹，那麼請嘗試一下：
        - 跳過刪除函數，直接實現搜索和插入功能
    - 我希望能閱讀到更多關於 B 樹的資料，因為它也被廣泛地應用到大型的數據庫當中。
    - [ ] [自平衡二叉查找樹](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree)

    - [ ] **AVL 樹**
        - 實際中：我能告訴你的是，該種樹並無太多的用途，但我能看到有用的地方在哪裡：AVL 樹是另一種平衡查找樹結構。其可支持時間複雜度為 O(log n) 的查詢、插入及刪除。它比紅黑樹嚴格意義上更為平衡，從而導致插入和刪除更慢，但遍歷卻更快。正因如此，才彰顯其結構的魅力。只需要構建一次，就可以在不重新構造的情況下讀取，適合於實現諸如語言字典（或程序字典，如一個彙編程序或解釋程序的操作碼）。
        - [ ] [MIT AVL 樹 / AVL 樹的排序（視頻）](https://www.youtube.com/watch?v=FNeL18KsWPc&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=6)
        - [ ] [AVL 樹（視頻）](https://www.coursera.org/learn/data-structures/lecture/Qq5E0/avl-trees)
        - [ ] [AVL 樹的實現（視頻）](https://www.coursera.org/learn/data-structures/lecture/PKEBC/avl-tree-implementation)
        - [ ] [分離與合併](https://www.coursera.org/learn/data-structures/lecture/22BgE/split-and-merge)

    - [ ] **伸展樹**
        - 實際中：伸展樹一般用於緩存、內存分配者、路由器、垃圾回收者、數據壓縮、ropes（字符串的一種替代品，用於存儲長串的文本字符）、Windows NT（虛擬內存、網絡及文件系統）等的實現。
        - [ ] [CS 61B：伸展樹（Splay trees）（視頻）](https://www.youtube.com/watch?v=Najzh1rYQTo&index=23&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)
        - [ ] MIT 教程：伸展樹（Splay trees）：
            - 該教程會過於學術，但請觀看到最後的10分鐘以​​確保掌握。
            - [視頻](https://www.youtube.com/watch?v=QnPl_Y6EqMo)

    - [ ] **2-3查找樹**
        - 實際中：2-3樹的元素插入非常快速，但卻有著查詢慢的代價（因為相比較 AVL 樹來說，其高度更高）。
        - 你會很少用到2-3樹。這是因為，其實現過程中涉及到不同類型的節點。因此，人們更多地會選擇紅黑樹。
        - [ ] [2-3樹的直感與定義（視頻）](https://www.youtube.com/watch?v=C3SsdUqasD4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=2)
        - [ ] [2-3樹的二元觀點](https://www.youtube.com/watch?v=iYvBtGKsqSg&index=3&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [2-3樹（學生敘述）（視頻）](https://www.youtube.com/watch?v=TOb1tuEZ2X4&index=5&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

    - [ ] **2-3-4樹 (亦稱2-4樹)**
        - 實際中：對於每一棵2-4樹，都有著對應的紅黑樹來存儲同樣順序的數據元素。在2-4樹上進行插入及刪除操作等同於在紅黑樹上進行顏色翻轉及輪換。這使得2-4樹成為一種用於掌握紅黑樹背後邏輯的重要工具。這就是為什麼許多算法引導文章都會在介紹紅黑樹之前，先介紹2-4樹，儘管**2-4樹在實際中並不經常使用**。
        - [ ] [CS 61B Lecture 26：平衡查找樹（視頻）](https://www.youtube.com/watch?v=zqrqYXkth6Q&index=26&list=PL4BBB74C7D2A1049C)
        - [ ] [自底向上的2-4樹（視頻）](https://www.youtube.com/watch?v=DQdMYevEyE4&index=4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [自頂向下的2-4樹（視頻）](https://www.youtube.com/watch?v=2679VQ26Fp4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=5)

    - [ ] **B 樹**
        - 有趣的是：為啥叫 B 仍然是一個神秘。因為 B 可代表波音（Boeing）、平衡（Balanced）或 Bayer（聯合創造者）
        - 實際中：B 樹會被廣泛適用於數據庫中，而現代大多數的文件系統都會使用到這種樹（或變種)。除了運用在數據庫中，B 樹也會被用於文件系統以快速訪問一個文件的任意塊。但存在著一個基本的問題，那就是如何將文件塊 i 轉換成一個硬盤塊（或一個柱面-磁頭-扇區）上的地址。
        - [ ] [B 樹](https://en.wikipedia.org/wiki/B-tree)
        - [ ] [B 樹的介紹（視頻）](https://www.youtube.com/watch?v=I22wEC1tTGo&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=6)
        - [ ] [B 樹的定義及其插入操作（視頻）](https://www.youtube.com/watch?v=s3bCdZGrgpA&index=7&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [B 樹的刪除操作（視頻）](https://www.youtube.com/watch?v=svfnVhJOfMc&index=8&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [MIT 6.851 —— 內存層次模塊（Memory Hierarchy Models）（視頻）](https://www.youtube.com/watch?v=V3omVLzI0WE&index=7&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)
            - 覆蓋有高速緩存參數無關型（cache-oblivious）B 樹和非常有趣的數據結構
            - 頭37分鐘講述的很專業，或許可以跳過（B 指塊的大小、即緩存行的大小）

    - [ ] **紅黑樹**
        - 實際中：紅黑樹提供了在最壞情況下插入操作、刪除操作和查找操作的時間保證。這些時間值的保障不僅對時間敏感型應用有用，例如實時應用，還對在其他數據結構中塊的構建非常有用，而這些數據結構都提供了最壞情況下的保障；例如，許多用於計算幾何學的數據結構都可以基於紅黑樹，而目前Linux 系統所採用的完全公平調度器（the Completely Fair Scheduler）也使用到了該種樹。在 Java 8中，紅黑樹也被用於存儲哈希列表集合中相同的數據，而不是使用鍊錶及哈希碼。
        - [ ] [Aduni —— 算法 —— 課程4（該鏈接直接跳到開始部分）（視頻）](https://youtu.be/1W3x0f_RmUo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3871)
        - [ ] [Aduni —— 算法 —— 課程5（視頻）](https://www.youtube.com/watch?v=hm2GHwyKF1o&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=5)
        - [ ] [黑樹（Black Tree）](https://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
        - [ ] [二分查找及紅黑樹的介紹](https://www.topcoder.com/community/data-science/data-science-tutorials/an-introduction-to-binary-search-and-red- black-trees/)

- ### N 叉樹（K 叉樹、M 叉樹）
    - 注意：N 或 K 指的是分支係數（即樹的最大分支數）：
        - 二叉樹是一種分支係數為2的樹
        - 2-3樹是一種分支係數為3的樹
    - [ ] [K 叉樹](https://en.wikipedia.org/wiki/K-ary_tree)

## 排序（Sorting）

- [ ] 筆記:
    - 實現各種排序 & 知道每種排序的最壞、最好和平均的複雜度分別是什麼場景:
        - 不要用冒泡排序 - 大多數情況下效率感人 - 時間複雜度 O(n^2), 除非 n <= 16
    - [ ] 排序算法的穩定性 ("快排是穩定的麼?")
        - [排序算法的穩定性](https://en.wikipedia.org/wiki/Sorting_algorithm#Stability)
        - [排序算法的穩定性](http://stackoverflow.com/questions/1517793/stability-in-sorting-algorithms)
        - [排序算法的穩定性](http://stackoverflow.com/questions/1517793/stability-in-sorting-algorithms)
        - [排序算法的穩定性](http://www.geeksforgeeks.org/stability-in-sorting-algorithms/)
        - [排序算法 - 穩定性](http://homepages.math.uic.edu/~leon/cs-mcs401-s08/handouts/stability.pdf)
    - [ ] 哪種排序算法可以用鍊錶？哪種用數組？哪種兩者都可？
        - 並不推薦對一個鍊錶排序，但歸併排序是可行的.
        - [鍊錶的歸併排序](http://www.geeksforgeeks.org/merge-sort-for-linked-list/)

- 關於堆排序，請查看前文堆的數據結構部分。堆排序很強大，不過是非穩定排序。

- [ ] [冒泡排序 (video)](https://www.youtube.com/watch?v=P00xJgWzz2c&index=1&list=PL89B61F78B552C1AB)
- [ ] [冒泡排序分析 (video)](https://www.youtube.com/watch?v=ni_zk257Nqo&index=7&list=PL89B61F78B552C1AB)
- [ ] [插入排序 & 歸併排序 (video)](https://www.youtube.com/watch?v=Kg4bqzAqRBM&index=3&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
- [ ] [插入排序 (video)](https://www.youtube.com/watch?v=c4BRHC7kTaQ&index=2&list=PL89B61F78B552C1AB)
- [ ] [歸併排序 (video)](https://www.youtube.com/watch?v=GCae1WNvnZM&index=3&list=PL89B61F78B552C1AB)
- [ ] [快排 (video)](https://www.youtube.com/watch?v=y_G9BkAm6B8&index=4&list=PL89B61F78B552C1AB)
- [ ] [選擇排序 (video)](https://www.youtube.com/watch?v=6nDMgr0-Yyo&index=8&list=PL89B61F78B552C1AB)

- [ ] 斯坦福大學關於排序算法的視頻:
    - [ ] [課程 15 | 編程抽象 (video)](https://www.youtube.com/watch?v=ENp00xylP7c&index=15&list=PLFE6E58F856038C69)
    - [ ] [課程 16 | 編程抽象 (video)](https://www.youtube.com/watch?v=y4M9IVgrVKo&index=16&list=PLFE6E58F856038C69)

- [ ] Shai Simonson 視頻, [Aduni.org](http://www.aduni.org/):
    - [ ] [算法 - 排序 - 第二講 (video)](https://www.youtube.com/watch?v=odNJmw5TOEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=2)
    - [ ] [算法 - 排序2 - 第三講 (video)](https://www.youtube.com/watch?v=hj8YKFTFKEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=3)

- [ ] Steven Skiena 關於排序的視頻:
    - [ ] [課程從 26:46 開始 (video)](https://youtu.be/ute-pmMkyuk?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1600)
    - [ ] [課程從 27:40 開始 (video)](https://www.youtube.com/watch?v=yLvp-pB8mak&index=8&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [課程從 35:00 開始 (video)](https://www.youtube.com/watch?v=q7K9otnzlfE&index=9&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [課程從 23:50 開始 (video)](https://www.youtube.com/watch?v=TvqIGu9Iupw&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=10)

- [ ] 加州大學伯克利分校（UC Berkeley） 大學課程:
    - [ ] [CS 61B 課程 29: 排序 I (video)](https://www.youtube.com/watch?v=EiUvYS2DT6I&list=PL4BBB74C7D2A1049C&index=29)
    - [ ] [CS 61B 課程 30: 排序 II (video)](https://www.youtube.com/watch?v=2hTY3t80Qsk&list=PL4BBB74C7D2A1049C&index=30)
    - [ ] [CS 61B 課程 32: 排序 III (video)](https://www.youtube.com/watch?v=Y6LOLpxg6Dc&index=32&list=PL4BBB74C7D2A1049C)
    - [ ] [CS 61B 課程 33: 排序 V (video)](https://www.youtube.com/watch?v=qNMQ4ly43p4&index=33&list=PL4BBB74C7D2A1049C)

- [ ] - 歸併排序:
    - [ ] [使用外部數組](http://www.cs.yale.edu/homes/aspnes/classes/223/examples/sorting/mergesort.c)
    - [ ] [對原數組直接排序](https://github.com/jwasham/practice-cpp/blob/master/merge_sort/merge_sort.cc)
- [ ] - 快速排序:
    - [ ] [實現](http://www.cs.yale.edu/homes/aspnes/classes/223/examples/randomization/quick.c)
    - [ ] [實現](https://github.com/jwasham/practice-c/blob/master/quick_sort/quick_sort.c)

- [ ] 實現:
    - [ ] 歸併：平均和最差情況的時間複雜度為 O(n log n)。
    - [ ] 快排：平均時間複雜度為 O(n log n)。
    - 選擇排序和插入排序的最壞、平均時間複雜度都是 O(n^2)。
    - 關於堆排序，請查看前文堆的數據結構部分。

- [ ] 有興趣的話，還有一些補充 - 但並不是必須的:
    - [ ] [基數排序](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#radixSort)
    - [ ] [基數排序 (video)](https://www.youtube.com/watch?v=xhr26ia4k38)
    - [ ] [基數排序, 計數排序 (線性時間內) (video)](https://www.youtube.com/watch?v=Nz1KZXbghj8&index=7&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [隨機算法: 矩陣相乘, 快排, Freivalds' 算法 (video)](https://www.youtube.com/watch?v=cNB2lADK3_s&index=8&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [線性時間內的排序 (video)](https://www.youtube.com/watch?v=pOKy3RZbSws&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=14)

## 圖（Graphs）

圖論能解決計算機科學裡的很多問題，所以這一節會比較長，像樹和排序的部分一樣。

- Yegge 的筆記:
    - 有 3 種基本方式在內存裡表示一個圖:
        - 對象和指針
        - 矩陣
        - 鄰接表
    - 熟悉以上每一種圖的表示法，並了解各自的優缺點
    - 寬度優先搜索和深度優先搜索 - 知道它們的計算複雜度和設計上的權衡以及如何用代碼實現它們
    - 遇到一個問題時，首先嘗試基於圖的解決方案，如果沒有再去嘗試其他的。

- [ ] Skiena 教授的課程 - 很不錯的介紹:
    - [ ] [CSE373 2012 - 課程 11 - 圖的數據結構 (video)](https://www.youtube.com/watch?v=OiXxhDrFruw&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=11)
    - [ ] [CSE373 2012 - 課程 12 - 廣度優先搜索 (video)](https://www.youtube.com/watch?v=g5vF8jscteo&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=12)
    - [ ] [CSE373 2012 - 課程 13 - 圖的算法 (video)](https://www.youtube.com/watch?v=S23W6eTcqdY&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=13)
    - [ ] [CSE373 2012 - 課程 14 - 圖的算法 (1) (video)](https://www.youtube.com/watch?v=WitPBKGV0HY&index=14&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [CSE373 2012 - 課程 15 - 圖的算法 (2) (video)](https://www.youtube.com/watch?v=ia1L30l7OIg&index=15&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [CSE373 2012 - 課程 16 - 圖的算法 (3) (video)](https://www.youtube.com/watch?v=jgDOQq6iWy8&index=16&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)

- [ ] 圖 (複習和其他):

    - [ ] [6.006 單源最短路徑問題 (video)](https://www.youtube.com/watch?v=Aa2sqUhIn-E&index=15&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.006 Dijkstra 算法 (video)](https://www.youtube.com/watch?v=2E7MmKv0Y24&index=16&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.006 Bellman-Ford 算法(video)](https://www.youtube.com/watch?v=ozsuci5pIso&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=17)
    - [ ] [6.006 Dijkstra 效率優化 (video)](https://www.youtube.com/watch?v=CHvQ3q_gJ7E&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=18)
    - [ ] [Aduni: 圖的算法I - 拓撲排序, 最小生成樹, Prim 算法- 第六課(video)]( https://www.youtube.com/watch?v=i_AQT_XfvD8&index=6&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm )
    - [ ] [Aduni: 圖的算法II - 深度優先搜索, 廣度優先搜索, Kruskal 算法, 並查集數據結構- 第七課(video)]( https://www.youtube.com/watch?v= ufj5_bppBsA&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=7)
    - [ ] [Aduni: 圖的算法 III: 最短路徑 - 第八課 (video)](https://www.youtube.com/watch?v=DiedsPsMKXc&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=8)
    - [ ] [Aduni: 圖的算法. IV: 幾何算法介紹 - 第九課 (video)](https://www.youtube.com/watch?v=XIAQRlNkJAw&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=9)
    - [ ] [CS 61B 2014 (從 58:09 開始) (video)](https://youtu.be/dgjX4HdMI-Q?list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&t=3489)
    - [ ] [CS 61B 2014: 加權圖 (video)](https://www.youtube.com/watch?v=aJjlQCFwylA&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=19)
    - [ ] [貪心算法: 最小生成樹 (video)](https://www.youtube.com/watch?v=tKwnms5iRBU&index=16&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [圖的算法之強連通分量 Kosaraju 算法 (video)](https://www.youtube.com/watch?v=RpgcYiky7uw)

- 完整的 Coursera 課程:
    - [ ] [圖的算法 (video)](https://www.coursera.org/learn/algorithms-on-graphs/home/welcome)

- Yegge: 如果有機會，可以試試研究更酷炫的算法:
    - [ ] Dijkstra 算法 - 上文 - 6.006
    - [ ] A* 算法
        - [ ] [A* 算法](https://en.wikipedia.org/wiki/A*_search_algorithm)
        - [ ] [A* 尋路教程 (video)](https://www.youtube.com/watch?v=KNXfSOx4eEE)
        - [ ] [A* 尋路 (E01: 算法解釋) (video)](https://www.youtube.com/watch?v=-L-WgKMFuhE)

- 我會實現:
    - [ ] DFS 鄰接表 (遞歸)
    - [ ] DFS 鄰接表 (棧迭代)
    - [ ] DFS 鄰接矩陣 (遞歸)
    - [ ] DFS 鄰接矩陣 (棧迭代)
    - [ ] BFS 鄰接表
    - [ ] BFS 鄰接矩陣
    - [ ] 單源最短路徑問題 (Dijkstra)
    - [ ] 最小生成樹
    - 基於 DFS 的算法 (根據上文 Aduni 的視頻):
        - [ ] 檢查環 (我們會先檢查是否有環存在以便做拓撲排序)
        - [ ] 拓撲排序
        - [ ] 計算圖中的連通分支
        - [ ] 列出強連通分量
        - [ ] 檢查雙向圖

可以從 Skiena 的書（參考下面的書推薦小節）和麵試書籍中學習更多關於圖的實踐。

## 更多知識

- ### 遞歸（Recursion）
    - [ ] Stanford 大學關於遞歸 & 回溯的課程:
        - [ ] [課程 8 | 抽象編程 (video)](https://www.youtube.com/watch?v=gl3emqCuueQ&list=PLFE6E58F856038C69&index=8)
        - [ ] [課程 9 | 抽象編程 (video)](https://www.youtube.com/watch?v=uFJhEPrbycQ&list=PLFE6E58F856038C69&index=9)
        - [ ] [課程 10 | 抽象編程 (video)](https://www.youtube.com/watch?v=NdF1QDTRkck&index=10&list=PLFE6E58F856038C69)
        - [ ] [課程 11 | 抽象編程 (video)](https://www.youtube.com/watch?v=p-gpaIGRCQI&list=PLFE6E58F856038C69&index=11)
    - 什麼時候適合使用
    - 尾遞歸會更好麼?
        - [ ] [什麼是尾遞歸以及為什麼它如此糟糕?](https://www.quora.com/What-is-tail-recursion-Why-is-it-so-bad)
        - [ ] [尾遞歸 (video)](https://www.youtube.com/watch?v=L1jjXGfxozc)

- ### 動態規劃（Dynamic Programming）
    - **注意** ：動態規劃是門極為重要的技術，儘管其並未被Google 提供的準備手冊提及，但你可能會對尋求最佳解的方式有點疑問，所以我將其列入這份表單。
    - 這一部分會有點困難，每個可以用動態規劃解決的問題都必須先定義出遞推關係，要推導出來可能會有點棘手。
    - 我建議先閱讀和學習足夠多的動態規劃的例子，以便對解決 DP 問題的一般模式有個紮實的理解。

    - [ ] 視頻:
        - Skiena 的視頻可能會有點難跟上，有時候他用白板寫的字會比較小，難看清楚。
        - [ ] [Skiena: CSE373 2012 - 課程 19 - 動態規劃介紹 (video)](https://youtu.be/Qc2ieXRgR0k?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1718)
        - [ ] [Skiena: CSE373 2012 - 課程 20 - 編輯距離 (video)](https://youtu.be/IsmMhMdyeGY?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=2749)
        - [ ] [Skiena: CSE373 2012 - 課程 21 - 動態規劃舉例 (video)](https://youtu.be/o0V9eYF4UI8?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=406)
        - [ ] [Skiena: CSE373 2012 - 課程 22 - 動態規劃應用 (video)](https://www.youtube.com/watch?v=dRbMC1Ltl3A&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=22)
        - [ ] [Simonson: 動態規劃 0 (starts at 59:18) (video)](https://youtu.be/J5aJEcOr6Eo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3558)
        - [ ] [Simonson: 動態規劃 I - 課程 11 (video)](https://www.youtube.com/watch?v=0EzHjQ_SOeU&index=11&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [Simonson: 動態規劃 II - 課程 12 (video)](https://www.youtube.com/watch?v=v1qiRwuJU7g&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=12)
        - [ ] 單獨的 DP 問題 (每一個視頻都很短):
            [動態規劃 (video)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)
    - [ ] Yale 課程筆記:
        - [ ] [動態規劃](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#dynamicProgramming)
    - [ ] Coursera 課程:
        - [ ] [RNA 二級結構問題 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/80RrW/the-rna-secondary-structure-problem)
        - [ ] [動態規划算法 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/PSonq/a-dynamic-programming-algorithm)
        - [ ] [DP 算法描述 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/oUEK2/illustrating-the-dp-algorithm)
        - [ ] [DP 算法的運行時間 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/nfK2r/running-time-of-the-dp-algorithm)
        - [ ] [DP vs 遞歸實現 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/M999a/dp-vs-recursive-implementation)
        - [ ] [全局成對序列排列 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/UZ7o6/global-pairwise-sequence-alignment)
        - [ ] [本地成對序列排列 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/WnNau/local-pairwise-sequence-alignment)

- ### 組合（Combinatorics） (n 中選 k 個) & 概率（Probability）
    - [ ] [數據技巧: 如何找出階乘、排列和組合(選擇) (video)](https://www.youtube.com/watch?v=8RRo6Ti9d0U)
    - [ ] [來點學校的東西: 概率 (video)](https://www.youtube.com/watch?v=sZkAAk9Wwa4)
    - [ ] [來點學校的東西: 概率和馬爾可夫鏈 (video)](https://www.youtube.com/watch?v=dNaJg-mLobQ)
    - [ ] 可汗學院:
        - 課程設置:
            - [ ] [概率理論基礎](https://www.khanacademy.org/math/probability/probability-and-combinatorics-topic)
        - 視頻 - 41 (每一個都短小精悍):
            - [ ] [概率解釋 (video)](https://www.youtube.com/watch?v=uzkc-qNVoOk&list=PLC58778F28211FA19)

- ### NP, NP-完全和近似算法
    - 知道最經典的一些 NP 完全問題，比如旅行商問題和背包問題,
        而且能在面試官試圖忽悠你的時候識別出他們。
    - 知道 NP 完全是什麼意思.
    - [ ] [計算複雜度 (video)](https://www.youtube.com/watch?v=moPtwq_cVH8&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=23)
    - [ ] Simonson:
        - [ ] [貪心算法. II & 介紹 NP-完全性 (video)](https://youtu.be/qcGnJ47Smlo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=2939)
        - [ ] [NP-完全性 II & 歸約 (video)](https://www.youtube.com/watch?v=e0tGC6ZQdQE&index=16&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [NP-完全性 III (Video)](https://www.youtube.com/watch?v=fCX1BGT3wjE&index=17&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [NP-完全性 IV (video)](https://www.youtube.com/watch?v=NKLDp3Rch3M&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=18)
    - [ ] Skiena:
        - [ ] [CSE373 2012 - 課程 23 - 介紹 NP-完全性 IV (video)](https://youtu.be/KiK5TVgXbFg?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1508)
        - [ ] [CSE373 2012 - 課程 24 - NP-完全性證明 (video)](https://www.youtube.com/watch?v=27Al52X3hd4&index=24&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
        - [ ] [CSE373 2012 - 課程 25 - NP-完全性挑戰 (video)](https://www.youtube.com/watch?v=xCPH4gwIIXM&index=25&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [複雜度: P, NP, NP-完全性, 規約 (video)](https://www.youtube.com/watch?v=eHZifpgyH_4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=22)
    - [ ] [複雜度: 近視算法 Algorithms (video)](https://www.youtube.com/watch?v=MEz1J9wY2iM&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=24)
    - [ ] [複雜度: 固定參數算法 (video)](https://www.youtube.com/watch?v=4q-jmGrmxKs&index=25&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - Peter Norvik 討論旅行商問題的近似最優解:
        - [Jupyter 筆記本](http://nbviewer.jupyter.org/url/norvig.com/ipython/TSP.ipynb)
    - 《算法導論》的第 1048 - 1140 頁。

- ### 緩存（Cache）
    - [ ] LRU 緩存:
        - [ ] [LRU 的魔力 (100 Days of Google Dev) (video)](https://www.youtube.com/watch?v=R5ON3iwx78M)
        - [ ] [實現 LRU (video)](https://www.youtube.com/watch?v=bq6N7Ym81iI)
        - [ ] [LeetCode - 146 LRU Cache (C++) (video)](https://www.youtube.com/watch?v=8-FZRAjR7qU)
    - [ ] CPU 緩存:
        - [ ] [MIT 6.004 L15: 存儲體系 (video)](https://www.youtube.com/watch?v=vjYF_fAZI5E&list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-&index=24)
        - [ ] [MIT 6.004 L16: 緩存的問題 (video)](https://www.youtube.com/watch?v=ajgC3-pyGlk&index=25&list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-)

- ### 進程（Processe）和線程（Thread）
    - [ ] 計算機科學 162 - 操作系統 (25 個視頻):
        - 視頻 1-11 是關於進程和線程
        - [操作系統和系統編程 (video)](https://www.youtube.com/playlist?list=PL-XXv-cvA_iBDyz-ba4yDskqMDY6A1w_c)
    - [進程和線程的區別是什麼?](https://www.quora.com/What-is-the-difference-between-a-process-and-a-thread)
    - 涵蓋了:
        - 進程、線程、協程
            - 進程和線程的區別
            - 進程
            - 線程
            - 鎖
            - 互斥
            - 信號量
            - 監控
            - 他們是如何工作的
            - 死鎖
            - 活鎖
        - CPU 活動, 中斷, 上下文切換
        - 現代多核處理器的並發式結構
        - 進程資源需要（內存：代碼、靜態存儲器、棧、堆、文件描述符、I/O）
        - 線程資源需要（在同一個進程內和其他線程共享以上的資源，但是每個線程都有獨立的程序計數器、棧計數器、寄存器和棧）
        - Fork 操作是真正的寫時復制（只讀），直到新的進程寫到內存中，才會生成一份新的拷貝。
        - 上下文切換
            - 操作系統和底層硬件是如何初始化上下文切換的。
    - [ ] [C++ 的線程 (系列 - 10 個視頻)](https://www.youtube.com/playlist?list=PL5jc9xFGsL8E12so1wlMS0r0hTQoJL74M)
    - [ ] Python 的協程 (視頻):
        - [ ] [線程系列](https://www.youtube.com/playlist?list=PL1H1sBF1VAKVMONJWJkmUh6_p8g4F2oy1)
        - [ ] [Python 線程](https://www.youtube.com/watch?v=Bs7vPNbB9JM)
        - [ ] [理解 Python 的 GIL (2010)](https://www.youtube.com/watch?v=Obt-vMVdM8s)
            - [參考](http://www.dabeaz.com/GIL)
        - [ ] [David Beazley - Python 協程 - PyCon 2015](https://www.youtube.com/watch?v=MCs5OvhV9S4)
        - [ ] [Keynote David Beazley - 興趣主題 (Python 異步 I/O)](https://www.youtube.com/watch?v=ZzfHjytDceU)
        - [ ] [Python 中的互斥](https://www.youtube.com/watch?v=0zaPs8OtyKY)


    系統設計以及可伸縮性，要把軟硬件的伸縮性設計的足夠好有很多的東西要考慮，所以這是個包含非常多內容和資源的大主題。需要花費相當多的時間在這個主題上。

- ### 系統設計、可伸縮性、數據處理
    - Yegge 的注意事項:
        - 伸縮性
            - 把大數據集提取為單一值
            - 大數據集轉換
            - 處理大量的數據集
        - 系統
            - 特徵集
            - 接口
            - 類層次結構
            - 在特定的約束下設計系統
            - 輕量和健壯性
            - 權衡和折衷
            - 性能分析和優化
    - [ ] **從這裡開始**: [HiredInTech：系統設計](http://www.hiredintech.com/system-design/)
    - [ ] [該如何為技術面試裡設計方面的問題做準備?](https://www.quora.com/How-do-I-prepare-to-answer-design-questions-in-a-technical -interview?redirected_qid=1500023)
    - [ ] [在系統設計面試前必須知道的8 件事](http://blog.gainlo.co/index.php/2015/10/22/8-things-you-need-to-know-before -system-design-interviews/)
    - [ ] [算法設計](http://www.hiredintech.com/algorithm-design/)
    - [ ] [數據庫範式 - 1NF, 2NF, 3NF and 4NF (video)](https://www.youtube.com/watch?v=UrYLYV7WSHM)
    - [ ] [系統設計面試](https://github.com/checkcheckzz/system-design-interview) - 這一部分有很多的資源，瀏覽一下我放在下面的文章和例子。
    - [ ] [如何在系統設計面試中脫穎而出](http://www.palantir.com/2011/10/how-to-rock-a-systems-design-interview/)
    - [ ] [每個人都該知道的一些數字](http://everythingisdata.wordpress.com/2009/10/17/numbers-everyone-should-know/)
    - [ ] [上下文切換操作會耗費多少時間?](http://blog.tsunanet.net/2010/11/how-long-does-it-take-to-make-context.html)
    - [ ] [跨數據中心的事務 (video)](https://www.youtube.com/watch?v=srOgpXECblk)
    - [ ] [簡明 CAP 理論介紹](http://ksat.me/a-plain-english-introduction-to-cap-theorem/)
    - [ ] Paxos 一致性算法:
        - [時間很短](https://www.youtube.com/watch?v=s8JqcZtvnsM)
        - [用例 和 multi-paxos](https://www.youtube.com/watch?v=JEpsBg0AO6o)
        - [論文](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)
    - [ ] [一致性哈希](http://www.tom-e-white.com/2007/11/consistent-hashing.html)
    - [ ] [NoSQL 模式](http://horicky.blogspot.com/2009/11/nosql-patterns.html)
    - [ ] [OOSE: UML 2.0 系列 (video)](https://www.youtube.com/watch?v=OkC7HKtiZC0&list=PLGLfVvz_LVvQ5G-LdJ8RLqe-ndo7QITYc)
    - [ ] OOSE: 使用 UML 和 Java 開發軟件 (21 videos):
        - 如果你對 OO 都深刻的理解和實踐，可以跳過這部分。
        - [OOSE: 使用 UML 和 Java 開發軟件](https://www.youtube.com/playlist?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)
    - [ ] 面向對象編程的 SOLID 原則:
        - [ ] [Bob Martin 面向對象的 SOLID 原則和敏捷設計 (video)](https://www.youtube.com/watch?v=TMuno5RZNeE)
        - [ ] [C# SOLID 設計模式 (video)](https://www.youtube.com/playlist?list=PL8m4NUhTQU48oiGCSgCP1FiJEcg_xJzyQ)
        - [ ] [SOLID 原則 (video)](https://www.youtube.com/playlist?list=PL4CE9F710017EA77A)
        - [ ] S - [單一職責原則](http://www.oodesign.com/single-responsibility-principle.html) | [每個對象的單一職責](http://www.javacodegeeks.com/2011 /11/solid-single-responsibility-principle.html)
            - [更多](https://docs.google.com/open?id=0ByOwmqah_nuGNHEtcU5OekdDMkk)
        - [ ] O - [開閉原則](http://www.oodesign.com/open-close-principle.html) | [生產環境裡的對象應該為擴展做準備而不是為更改](https:/ /en.wikipedia.org/wiki/Open/closed_principle)
            - [更多](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgN2M5MTkwM2EtNWFkZC00ZTI3LWFjZTUtNTFhZGZiYmUzODc1&hl=en)
        - [ ] L - [里氏代換原則](http://www.oodesign.com/liskov-s-substitution-principle.html) | [基類和繼承類遵循'IS A' 原則](http: //stackoverflow.com/questions/56860/what-is-the-liskov-substitution-principle)
            - [更多](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgNzAzZjA5ZmItNjU3NS00MzQ5LTkwYjMtMDJhNDU5ZTM0MTlh&hl=en)
        - [ ] I - [接口隔離原則](http://www.oodesign.com/interface-segregation-principle.html) | 客戶端被迫實現用不到的接口
            - [5 分鐘講解接口隔離原則 (video)](https://www.youtube.com/watch?v=3CtAfl7aXAQ)
            - [更多](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgOTViYjJhYzMtMzYxMC00MzFjLWJjMzYtOGJiMDc5N2JkYmJi&hl=en)
        - [ ] D -[依賴反轉原則](http://www.oodesign.com/dependency-inversion-principle.html) | 減少對象裡的依賴。
            - [什麼是依賴倒置以及它為什麼重要](http://stackoverflow.com/questions/62539/what-is-the-dependency-inversion-principle-and-why-is-it-important)
            - [更多](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgMjdlMWIzNGUtZTQ0NC00ZjQ5LTkwYzQtZjRhMDRlNTQ3ZGMz&hl=en)
    - [ ] 可伸縮性:
        - [ ] [很棒的概述 (video)](https://www.youtube.com/watch?v=-W9F__D3oY4)
        - [ ] 簡短系列:
            - [克隆](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
            - [數據庫](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
            - [緩存](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
            - [異步](http://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism)
        - [ ] [可伸縮的 Web 架構和分佈式系統](http://www.aosabook.org/en/distsys.html)
        - [ ] [錯誤的分佈式系統解釋](https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf)
        - [ ] [實用編程技術](http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html)
            - [extra: Google Pregel 圖形處理](http://horicky.blogspot.com/2010/07/google-pregel-graph-processing.html)
        - [ ] [Jeff Dean - 在 Goolge 構建軟件系統 (video)](https://www.youtube.com/watch?v=modXC5IWTJI)
        - [ ] [可伸縮系統架構設計介紹](http://lethain.com/introduction-to-architecting-systems-for-scale/)
        - [ ] [使用 App Engine 和雲存儲擴展面向全球用戶的手機遊戲架構實踐(video)](https://www.youtube.com/watch?v=9nWyWwY2Onc)
        - [ ] [How Google Does Planet-Scale Engineering for Planet-Scale Infra (video)](https://www.youtube.com/watch?v=H4vMcD7zKM0)
        - [ ] [算法的重要性](https://www.topcoder.com/community/data-science/data-science-tutorials/the-importance-of-algorithms/)
        - [ ] [分片](http://highscalability.com/blog/2009/8/6/an-unorthodox-approach-to-database-design-the-coming-of-the.html)
        - [ ] [Facebook 系統規模擴展實踐 (2009)](https://www.infoq.com/presentations/Scale-at-Facebook)
        - [ ] [Facebook 系統規模擴展實踐 (2012), "為 10 億用戶構建" (video)](https://www.youtube.com/watch?v=oodS71YtkGU)
        - [ ] [Long Game 工程實踐 - Astrid Atkinson Keynote(video)](https://www.youtube.com/watch?v=p0jGmgIrf_M&list=PLRXxvay_m8gqVlExPC5DG3TGWJTaBgqSA&index=4)
        - [ ] [30 分鐘看完YouTuBe 7 年系統擴展經驗](http://highscalability.com/blog/2012/3/26/7-years-of-youtube-scalability-lessons-in-30-minutes. html)
            - [video](https://www.youtube.com/watch?v=G-lGCC4KKok)
        - [ ] [PayPal 如何用8 台虛擬機扛住10 億日交易量系統](http://highscalability.com/blog/2016/8/15/how-paypal-scaled-to-billions-of-transactions -daily-using-ju.html)
        - [ ] [如何對大數據集去重](https://blog.clevertap.com/how-to-remove-duplicates-in-large-datasets/)
        - [ ] [Etsy 的擴展和工程文化探究 Jon Cowie (video)](https://www.youtube.com/watch?v=3vV4YiqKm1o)
        - [ ] [是什麼造就了 Amazon 自己的微服務架構](http://thenewstack.io/led-amazon-microservices-architecture/)
        - [ ] [壓縮還是不壓縮，是 Uber 面臨的問題](https://eng.uber.com/trip-data-squeeze/)
        - [ ] [異步 I/O Tarantool 隊列](http://highscalability.com/blog/2016/3/3/asyncio-tarantool-queue-get-in-the-queue.html)
        - [ ] [什麼時候應該用近視查詢處理?](http://highscalability.com/blog/2016/2/25/when-should-approximate-query-processing-be-used.html)
        - [ ] [Google 從單數據中心到故障轉移, 到本地多宿主架構的演變]( http://highscalability.com/blog/2016/2/23/googles-transition-from-single-datacenter-to- failover-to-an.html)
        - [ ] [Spanner](http://highscalability.com/blog/2012/9/24/google-spanners-most-surprising-revelation-nosql-is-out-and.html)
        - [ ] [Egnyte: 構建和擴展PB 級分佈式系統架構的經驗教訓](http://highscalability.com/blog/2016/2/15/egnyte-architecture-lessons-learned-in-building-and- scaling.html)
        - [ ] [機器學習驅動的編程: 新世界的新編程方式](http://highscalability.com/blog/2016/7/6/machine-learning-driven-programming-a-new-programming-for- a.html)
        - [ ] [日服務數百萬請求的圖像優化技術](http://highscalability.com/blog/2016/6/15/the-image-optimization-technology-that-serves-millions-of-re. html)
        - [ ] [Patreon 架構](http://highscalability.com/blog/2016/2/1/a-patreon-architecture-short.html)
        - [ ] [Tinder: 推薦引擎是如何決定下一個你將會看到誰的?](http://highscalability.com/blog/2016/1/27/tinder-how-does-one-of-the -largest-recommendation-engines-de.html)
        - [ ] [現代緩存設計](http://highscalability.com/blog/2016/1/25/design-of-a-modern-cache.html)
        - [ ] [Facebook 實時視頻流擴展](http://highscalability.com/blog/2016/1/13/live-video-streaming-at-facebook-scale.html)
        - [ ] [在Amazon AWS 上把服務擴展到1100 萬量級的新手教程](http://highscalability.com/blog/2016/1/11/a-beginners-guide-to-scaling-to-11 -million-users-on-amazons.html)
        - [ ] [對延時敏感的應用是否應該使用Docker?](http://highscalability.com/blog/2015/12/16/how-does-the-use-of-docker-effect-latency.html )
        - [ ] [AMP（Accelerated Mobile Pages）的存在是對Google 的威脅麼?](http://highscalability.com/blog/2015/12/14/does-amp-counter-an-existential-threat-to -google.html)
        - [ ] [360 度解讀 Netflix 技術棧](http://highscalability.com/blog/2015/11/9/a-360-degree-view-of-the-entire-netflix-stack.html)
        - [ ] [延遲無處不在 - 如何搞定它？ ](http://highscalability.com/latency-everywhere-and-it-costs-you-sales-how-crush-it)
        - [ ] [無服務器架構](http://martinfowler.com/articles/serverless.html)
        - [ ] [是什麼驅動著 Instagram: 上百個實例、幾十種技術](http://instagram-engineering.tumblr.com/post/13649370142/what-powers-instagram-hundreds-of-instances)
        - [ ] [Cinchcast 架構- 每天處理1500 小時的音頻](http://highscalability.com/blog/2012/7/16/cinchcast-architecture-producing-1500-hours-of-audio-every-d.html )
        - [ ] [Justin.Tv 實時視頻播放架構](http://highscalability.com/blog/2010/3/16/justintvs-live-video-broadcasting-architecture.html)
        - [ ] [Playfish's 社交遊戲架構- 每月五千萬用戶增長](http://highscalability.com/blog/2010/9/21/playfishs-social-gaming-architecture-50-million-monthly-user. html)
        - [ ] [貓途鷹架構- 40 萬訪客, 200 萬動態頁面訪問, 30TB 數據](http://highscalability.com/blog/2011/6/27/tripadvisor-architecture-40m-visitors-200m-dynamic -page-view.html)
        - [ ] [PlentyOfFish 架構](http://highscalability.com/plentyoffish-architecture)
        - [ ] [Salesforce 架構- 如何扛住13 億日交易量](http://highscalability.com/blog/2013/9/23/salesforce-architecture-how-they-handle-13-billion-transacti.html )
        - [ ] [ESPN's 架構擴展](http://highscalability.com/blog/2013/11/4/espns-architecture-at-scale-operating-at-100000-duh-nuh-nuhs.html)
        - [ ] 下面 『消息、序列化和消息系統』部分的內容會提到什麼樣的技術能把各種服務整合到一起
        - [ ] Twitter:
            - [O'Reilly MySQL CE 2011: Jeremy Cole, "Big and Small Data at @Twitter" (video)](https://www.youtube.com/watch?v=5cKTP36HVgI)
            - [時間線的擴展](https://www.infoq.com/presentations/Twitter-Timeline-Scalability)
        - 更多內容可以查看視頻部分的『大規模數據挖掘』視頻系列。
    - [ ] 系統設計問題練習：下面有一些指導原則，每一個都有相關文檔以及在現實中該如何處理。
        - 複習: [HiredInTech 的系統設計](http://www.hiredintech.com/system-design/)
        - [cheat sheet](https://github.com/jwasham/coding-interview-university/blob/master/extras/cheat%20sheets/system-design.pdf)
        - 流程:
            1. 理解問題和範圍:
                - 在面試官的幫助下定義用例
                - 提出附加功能的建議
                - 去掉面試官認定範圍以外的內容
                - 假定高可用是必須的，而且要作為一個用例
            2. 考慮約束:
                - 問一下每月請求量
                - 問一下每秒請求量 (他們可能會主動提到或者讓你算一下)
                - 評估讀寫所佔的百分比
                - 評估的時候牢記 2/8 原則
                - 每秒寫多少數據
                - 總的數據存儲量要考慮超過 5 年的情況
                - 每秒讀多少數據
            3. 抽象設計:
                - 分層 (服務, 數據, 緩存)
                - 基礎設施: 負載均衡, 消息
                - 粗略的概括任何驅動整個服務的關鍵算法
                - 考慮瓶頸並指出解決方案
        - 練習:
            - [設計一個 CDN 網絡](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2112&context=compsci)
            - [設計一個隨機唯一 ID 生成系統](https://blog.twitter.com/2010/announcing-snowflake)
            - [設計一個在線多人卡牌遊戲](http://www.indieflashblog.com/how-to-create-an-asynchronous-multiplayer-game.html)
            - [設計一個 key-value 數據庫](http://www.slideshare.net/dvirsky/introduction-to-redis)
            - [設計一個函數獲取過去某個時間段內前 K 個最高頻訪問的請求]( https://icmi.cs.ucsb.edu/research/tech_reports/reports/2005-23.pdf)
            - [設計一個圖片分享系統](http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html)
            - [設計一個推薦系統](http://ijcai13.org/files/tutorial_slides/td3.pdf)
            - [設計一個短域名生成系統](http://www.hiredintech.com/system-design/the-system-design-process/)
            - [設計一個緩存系統](https://www.adayinthelifeof.nl/2011/02/06/memcache-internals/)

- ### 論文
    - 有 Google 的論文和一些知名的論文.
    - 你很可能實在沒時間一篇篇完整的讀完他們。我建議可以有選擇的讀其中一些論文裡的核心部分。
    - [ ] [1978: 通信順序處理](http://spinroot.com/courses/summer/Papers/hoare_1978.pdf)
        - [Go 實現](https://godoc.org/github.com/thomas11/csp)
        - [喜歡經典的論文?](https://www.cs.cmu.edu/~crary/819-f09/)
    - [ ] [2003: The Google 文件系統](http://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
        - 2012 年被 Colossus 取代了
    - [ ] [2004: MapReduce: Simplified Data Processing on Large Clusters]( http://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
        - 大多被雲數據流取代了?
    - [ ] [2007: 每個程序員都應該知道的內存知識 (非常長，作者建議跳過某些章節來閱讀)](https://www.akkadia.org/drepper/cpumemory.pdf)
    - [ ] [2012: Google 的 Colossus](https://www.wired.com/2012/07/google-colossus/)
        - 沒有論文
    - [ ] 2012: AddressSanitizer: 快速的內存訪問檢查器:
        - [論文](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/37752.pdf)
        - [視頻](https://www.usenix.org/conference/atc12/technical-sessions/presentation/serebryany)
    - [ ] 2013: Spanner: Google 的分佈式數據庫:
        - [論文](http://static.googleusercontent.com/media/research.google.com/en//archive/spanner-osdi2012.pdf)
        - [視頻](https://www.usenix.org/node/170855)
    - [ ] [2014: Machine Learning: The High-Interest Credit Card of Technical Debt](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43146.pdf)
    - [ ] [2015: Continuous Pipelines at Google](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43790.pdf)
    - [ ] [2015: 大規模高可用: 構建 Google Ads 的數據基礎設施](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44686.pdf)
    - [ ] [2015: TensorFlow: 異構分佈式系統上的大規模機器學習](http://download.tensorflow.org/paper/whitepaper2015.pdf )
    - [ ] [2015: 開發者應該如何搜索代碼：用例學習](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43835.pdf)
    - [ ] [2016: Borg, Omega, and Kubernetes](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44843.pdf)

- ### 測試
    - 涵蓋了:
        - 單元測試是如何工作的
        - 什麼是模擬對象
        - 什麼是集成測試
        - 什麼是依賴注入
    - [ ] [James Bach 講敏捷軟件測試 (video)](https://www.youtube.com/watch?v=SAhJf36_u5U)
    - [ ] [James Bach 軟件測試公開課 (video)](https://www.youtube.com/watch?v=ILkT_HV9DVU)
    - [ ] [Steve Freeman - 測試驅動的開發 (video)](https://vimeo.com/83960706)
        - [slides](http://gotocon.com/dl/goto-berlin-2013/slides/SteveFreeman_TestDrivenDevelopmentThatsNotWhatWeMeant.pdf)
    - [ ] [測試驅動的開發已死。測試不朽。 ](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)
    - [ ] [測試驅動的開發已死? (video)](https://www.youtube.com/watch?v=z9quxZsLcfo)
    - [ ] [視頻系列 (152 個) - 並不都是必須 (video)](https://www.youtube.com/watch?v=nzJapzxH_rE&list=PLAwxTw4SYaPkWVHeC_8aSIbSxE_NXI76g)
    - [ ] [Python：測試驅動的 Web 開發](http://www.obeythetestinggoat.com/pages/book.html#toc)
    - [ ] 依賴注入:
        - [ ] [視頻](https://www.youtube.com/watch?v=IKD2-MAkXyQ)
        - [ ] [測試之道](http://jasonpolites.github.io/tao-of-testing/ch3-1.1.html)
    - [ ] [如何編寫測試](http://jasonpolites.github.io/tao-of-testing/ch4-1.1.html)

- ### 調度
    - 在操作系統中是如何運作的
    - 在操作系統部分的視頻裡有很多資料

- ### 實現系統例程
    - 理解你使用的系統 API 底層有什麼
    - 你能自己實現它們麼?

- ### 字符串搜索和操作
    - [ ] [文本的搜索模式 (video)](https://www.coursera.org/learn/data-structures/lecture/tAfHI/search-pattern-in-text)
    - [ ] Rabin-Karp (videos):
        - [Rabin Karps 算法](https://www.coursera.org/learn/data-structures/lecture/c0Qkw/rabin-karps-algorithm)
        - [預先計算的優化](https://www.coursera.org/learn/data-structures/lecture/nYrc8/optimization-precomputation)
        - [優化: 實現和分析](https://www.coursera.org/learn/data-structures/lecture/h4ZLc/optimization-implementation-and-analysis)
        - [Table Doubling, Karp-Rabin](https://www.youtube.com/watch?v=BRO7mVIFt08&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=9)
        - [滾動哈希](https://www.youtube.com/watch?v=w6nuXg0BISo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=32)
    - [ ] Knuth-Morris-Pratt (KMP) 算法:
        - [Pratt 算法](https://en.wikipedia.org/wiki/Knuth%E2%80%93Morris%E2%80%93Pratt_algorithm)
        - [教程: Knuth-Morris-Pratt (KMP) 字符串匹配算法](https://www.youtube.com/watch?v=2ogqPWJSftE)
    - [ ] Boyer–Moore 字符串搜索算法
        - [Boyer-Moore字符串搜索算法](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_string_search_algorithm)
        - [Boyer-Moore-Horspool 高級字符串搜索算法 (video)](https://www.youtube.com/watch?v=QDZpzctPf10)
    - [ ] [Coursera: 字符串的算法](https://www.coursera.org/learn/algorithms-on-strings/home/week/1)

---

## 終面

    這一部分有一些短視頻，你可以快速的觀看和復習大多數重要概念。
    這對經常性的鞏固很有幫助。

#### 綜述:

- [ ] 2-3 分鐘的短視頻系列 (23 個)
    - [Videos](https://www.youtube.com/watch?v=r4r1DZcx1cM&list=PLmVb1OknmNJuC5POdcDv5oCS7_OUkDgpj&index=22)
- [ ] 2-5 分鐘的短視頻系列 - Michael Sambol (18 個):
    - [Videos](https://www.youtube.com/channel/UCzDJwLWoYCUQowF_nG3m5OQ)

#### 排序:

- [ ] 歸併排序: https://www.youtube.com/watch?v=GCae1WNvnZM


## 書籍

### Google Coaching 裡提到的

**閱讀並做練習:**

- [ ] 算法設計手冊 (Skiena)
    - 書 (Kindle 上可以租到):
        - [Algorithm Design Manual](http://www.amazon.com/Algorithm-Design-Manual-Steven-Skiena/dp/1849967202)
    - Half.com 是一個資源豐富且性價比很高的在線書店.
    - 答案:
        - [解答](http://www.algorithm.cs.sunysb.edu/algowiki/index.php/The_Algorithms_Design_Manual_(Second_Edition))
        - [解答](http://blog.panictank.net/category/algorithmndesignmanualsolutions/page/2/)
    - [勘誤表](http://www3.cs.stonybrook.edu/~skiena/algorist/book/errata)

    read and do exercises from the books below. Then move to coding challenges (further down below)
    一旦你理解了每日計劃裡的所有內容，就去讀上面所列的書並完成練習，然後開始讀下面所列的書並做練習，之後就可以開始實戰寫代碼了（本文再往後的部分）

**首先閱讀:**
- [ ] [Programming Interviews Exposed: Secrets to Landing Your Next Job, 2nd Edition](http://www.wiley.com/WileyCDA/WileyTitle/productCd-047012167X.html)

**然後閱讀 (這本獲得了很多推薦， 但是不在 Google coaching 的文檔裡):**
- [ ] [Cracking the Coding Interview, 6th Edition](http://www.amazon.com/Cracking-Coding-Interview-6th-Programming/dp/0984782850/)
    - 如果你看到有人在看 "The Google Resume", 實際上它和 "Cracking the Coding Interview" 是同一個作者寫的，而且後者是升級版。

### 附加書單

這些沒有被 Google 推薦閱讀，不過我因為需要這些背景知識所以也把它們列在了這裡。

- [ ] C Programming Language, Vol 2
    - [練習的答案](https://github.com/lekkas/c-algorithms)

- [ ] C++ Primer Plus, 6th Edition

- [ ] [《Unix 環境高級編程》 The Unix Programming Environment](http://product.half.ebay.com/The-UNIX-Programming-Environment-by-Brian-W-Kernighan-and-Rob-Pike- 1983-Other/54385&tg=info)

- [ ] [《編程珠璣》 Programming Pearls](http://www.amazon.com/Programming-Pearls-2nd-Jon-Bentley/dp/0201657880)

- [ ] [Algorithms and Programming: Problems and Solutions](http://www.amazon.com/Algorithms-Programming-Solutions-Alexander-Shen/dp/0817638474)

### 如果你有時間

- [ ] [Introduction to Algorithms](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844)

- [ ] [Elements of Programming Interviews](https://www.amazon.com/Elements-Programming-Interviews-Insiders-Guide/dp/1479274836)
    - 如果你希望在面試裡用 C++ 寫代碼，這本書的代碼全都是 C++ 寫的
    - 通常情況下能找到解決方案的好書.

## 編碼練習和挑戰

一旦你學會了理論基礎，就應該把它們拿出來練練。
盡量堅持每天做編碼練習，越多越好。

編程問題預備:

- [ ] [不錯的介紹 (摘自 System Design 章節): 算法設計:](http://www.hiredintech.com/algorithm-design/)
- [ ] [如何找到解決方案](https://www.topcoder.com/community/data-science/data-science-tutorials/how-to-find-a-solution/)
- [ ] [如何剖析 Topcoder 題目描述](https://www.topcoder.com/community/data-science/data-science-tutorials/how-to-dissect-a-topcoder-problem-statement/)
- [ ] [Topcoders 裡用到的數學](https://www.topcoder.com/community/data-science/data-science-tutorials/mathematics-for-topcoders/)
- [ ] [動態規劃 – 從入門到精通](https://www.topcoder.com/community/data-science/data-science-tutorials/dynamic-programming-from-novice-to-advanced/)

- [MIT 面試材料](https://courses.csail.mit.edu/iap/interview/materials.php)

- [針對編程語言本身的練習](http://exercism.io/languages)

編碼練習平台:

- [LeetCode](https://leetcode.com/)
- [TopCoder](https://www.topcoder.com/)
- [Project Euler (數學方向為主)](https://projecteuler.net/index.php?section=problems)
- [Codewars](http://www.codewars.com)
- [HackerRank](https://www.hackerrank.com/)
- [Codility](https://codility.com/programmers/)
- [InterviewCake](https://www.interviewcake.com/)
- [InterviewBit](https://www.interviewbit.com/invite/icjf)

- [模擬大公司的面試](http://www.gainlo.co/)

## 當你臨近面試時

- [ ] 搞定代碼面試 (videos):
    - [Cracking The Code Interview](https://www.youtube.com/watch?v=4NIb9l3imAo)
    - [Cracking the Coding Interview - 全棧系列](https://www.youtube.com/watch?v=Eg5-tdAwclo)
    - [Ask Me Anything: Gayle Laakmann McDowell (Cracking the Coding Interview 的作者)](https://www.youtube.com/watch?v=1fqxMuPmGak)

## 你的簡歷

- [10 條小貼士讓你寫出一份還算不錯的簡歷](http://steve-yegge.blogspot.co.uk/2007_09_01_archive.html)
- 這是搞定面試的第一個關鍵步驟


## 當面試來臨的時候

    隨著下面列舉的問題思考下你可能會遇到的 20 個面試問題
    每個問題準備 2-3 種回答
    準備點故事，不要只是擺一些你完成的事情的數據，相信我，人人都喜歡聽故事

- 你為什麼想得到這份工作？
- 你解決過的最有難度的問題是什麼？
- 面對過的最大挑戰是什麼?
- 見過的最好或者最壞的設計是怎麼樣的?
- 對某項 Google 產品提出改進建議。
- 你作為一個個體同時也是團隊的一員，如何達到最好的工作狀態?
- 你的什麼技能或者經驗是你的角色中不可或缺的?為什麼？
- 你在某份工作或某個項目中最享受的是什麼?
- 你在某份工作或某個項目中面臨過的最大挑戰是什麼?
- 你在某份工作或某個項目中遇到過的最蛋疼的 Bug 是什麼樣的？
- 你在某份工作或某個項目中學到了什麼？
- 你在某份工作或某個項目中哪些地方還可以做的更好？

## 問面試官的問題

    我會問的一些：(可能我已經知道了答案但我想听聽面試官的看法或者了解團隊的前景):

- 團隊多大規模?
- 開發週期是怎樣的? 會使用瀑布流/極限編程/敏捷開發麼?
- 經常會為 deadline 加班麼? 或者是有彈性的?
- 團隊裡怎麼做技術選型?
- 每周平均開多少次會?
- 你覺得工作環境有助於員工集中精力嗎?
- 目前正在做什麼工作?
- 喜歡這些事情嗎?
- 工作期限是怎麼樣的?

## 當你獲得了夢想的職位

我還能說些什麼呢，恭喜你！

- [我希望在Google 的第一天就知道的10 件事](https://medium.com/@moonstorming/10-things-i-wish-i-knew-on-my-first-day-at -google-107581d87286#.livxn7clw)

堅持繼續學習。

得到這份工作只是一個開始。

---

    ************************************************** ************************************************** *
    ************************************************** ************************************************** *

    下面的內容都是可選的。這些是我的推薦，不是 Google 的。
    通過學習這些內容，你將會得到更多的有關 CS 的概念，並將為所有的軟件工程工作做更好的準備。

    ************************************************** ************************************************** *
    ************************************************** ************************************************** *

---

## 附加的學習

- ### Unicode
    - [ ] [每一個軟件開發者的絕對最低限度，必須要知道的關於 Unicode 和字符集知識]( http://www.joelonsoftware.com/articles/Unicode.html)
    - [ ] [關於處理文本需要的編碼和字符集, 每個程序員絕對需要知道的知識](http://kunststube.net/encoding/)

- ### 字節順序
    - [ ] [大、小端字節序](https://www.cs.umd.edu/class/sum2003/cmsc311/Notes/Data/endian.html)
    - [ ] [大端字節 Vs 小端字節(視頻)](https://www.youtube.com/watch?v=JrNF0KRAlyo)
    - [ ] [大、小端字節序的里里外外(Big And Little Endian Inside/Out) (視頻)](https://www.youtube.com/watch?v=oBSuXP-1Tc0)
        - 內核開發者的討論非常技術性，如果大多數都超出了你的理解範圍，不要太擔心。
        - 前半段已經足夠了。

- ### Emacs and vi(m)
    - Yegge 的建議，從一個很早以前的亞馬遜招聘信息中而來：熟悉基於 unix 的代碼編輯器
    - vi(m):
        - [使用 vim 進行編輯 01 - 安裝, 設置和模式 (視頻)](https://www.youtube.com/watch?v=5givLEMcINQ&index=1&list=PL13bz4SHGmRxlZVmWQ9DvXo1fEg4UdGkr)
        - [VIM 的冒險之旅](http://vim-adventures.com/)
        - 4 個視頻集:
            - [vi/vim 編輯器 - 課程 1](https://www.youtube.com/watch?v=SI8TeVMX8pk)
            - [vi/vim 編輯器 - 課程 2](https://www.youtube.com/watch?v=F3OO7ZIOaJE)
            - [vi/vim 編輯器 - 課程 4](https://www.youtube.com/watch?v=1lYD5gwgZIA)
            - [vi/vim 編輯器 - 課程 3](https://www.youtube.com/watch?v=ZYEccA_nMaI)
        - [使用 Vi 而不是 Emacs](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Using_Vi_instead_of_Emacs)
    - emacs:
        - [基礎 Emacs 教程 (視頻)](https://www.youtube.com/watch?v=hbmV1bnQ-i0)
        - 3 個視頻集:
            - [Emacs 教程 (初學者) -第 1 部分- 文件命令, 剪切/複製/粘貼, 自定義命令](https://www.youtube.com/watch?v=ujODL7MD04Q)
            - [Emacs 教程 (初學者 -第 2 部分- Buffer 管理, 搜索, M-x grep 和 rgrep 模式](https://www.youtube.com/watch?v=XWpsRupJ4II)
            - [Emacs 教程 (初學者 -第 3 部分- 表達式, 聲明, ~/.emacs 文件和包機制](https://www.youtube.com/watch?v=paSgzPso-yc)
        - [Evil 模式: 或許, 我是怎樣對 Emacs 路人轉粉的 (視頻)](https://www.youtube.com/watch?v=JWD1Fpdd4Pc)
        - [使用 Emacs 開發 C 程序](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Writing_C_programs_with_Emacs)
        - [(或許) 深度組織模式:管理結構 (視頻)](https://www.youtube.com/watch?v=nsGYet02bEk)

- ### Unix 命令行工具
    - 下列內容中的優秀工具由的 Yegge 推薦，Yegge 目前致力於 Amazon 人事招聘處。
    - [ ] bash
    - [ ] cat
    - [ ] grep
    - [ ] sed
    - [ ] awk
    - [ ] curl or wget
    - [ ] sort
    - [ ] tr
    - [ ] uniq
    - [ ] [strace](https://en.wikipedia.org/wiki/Strace)
    - [ ] [tcpdump](https://danielmiessler.com/study/tcpdump/)

- ### 信息資源 (視頻)
    - [ ] [Khan Academy 可汗學院](https://www.khanacademy.org/computing/computer-science/informationtheory)
    - [ ] 更多有關馬爾可夫的內容:
        - [ ] [Core Markov Text Generation馬爾可夫內容生成](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/waxgx/core-markov-text-generation)
        - [ ] [Core Implementing Markov Text Generation馬爾可夫內容生成補充](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/gZhiC/core-implementing-markov-text-generation )
        - [ ] [Project = Markov Text Generation Walk Through一個馬爾可夫內容生成器的項目](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/EUjrq/project-markov- text-generation-walk-through)
    - 關於更多信息，請參照下方 MIT 6.050J 信息和系統複雜度的內容.

- ### 奇偶校驗位 & 漢明碼 (視頻)
    - [ ] [入門](https://www.youtube.com/watch?v=q-3BctoUpHE)
    - [ ] [奇偶校驗位](https://www.youtube.com/watch?v=DdMcAUlxh1M)
    - [ ] 漢明碼(Hamming Code):
        - [發現錯誤](https://www.youtube.com/watch?v=1A_NcXxdoCc)
        - [修正錯誤](https://www.youtube.com/watch?v=JAMLuxdHH8o)
    - [ ] [檢查錯誤](https://www.youtube.com/watch?v=wbH2VxzmoZk)

- ### 系統熵值（系統複雜度）
    - 請參考下方視頻
    - 觀看之前，請先確定觀看了信息論的視頻
    - [ ] [信息理論, 克勞德·香農, 熵值, 系統冗餘, 數據比特壓縮 (視頻)](https://youtu.be/JnJq3Py0dyM?t=176)

- ### 密碼學
    - 請參考下方視頻
    - 觀看之前，請先確定觀看了信息論的視頻
    - [ ] [可汗學院](https://www.khanacademy.org/computing/computer-science/密碼學)
    - [ ] [密碼學: 哈希函數](https://www.youtube.com/watch?v=KqqOXndnvic&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=30)
    - [ ] [密碼學: 加密](https://www.youtube.com/watch?v=9TNI2wHmaeI&index=31&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

- ### 壓縮
    - 觀看之前，請先確定觀看了信息論的視頻
    - [ ] 壓縮 (視頻):
        - [ ] [壓縮](https://www.youtube.com/watch?v=Lto-ajuqW3w)
        - [ ] [壓縮熵值](https://www.youtube.com/watch?v=M5c_RFKVkko)
        - [ ] [由上而下的樹 (霍夫曼編碼樹)](https://www.youtube.com/watch?v=umTbivyJoiI)
        - [ ] [額外比特 - 霍夫曼編碼樹](https://www.youtube.com/watch?v=DV8efuB3h2g)
        - [ ] [優雅的壓縮數據 (無損數據壓縮方法)](https://www.youtube.com/watch?v=goOa3DGezUA)
        - [ ] [Text Compression Meets Probabilities](https://www.youtube.com/watch?v=cCDCfoHTsaU)
    - [ ] [數據壓縮的藝術](https://www.youtube.com/playlist?list=PLOU2XLYxmsIJGErt5rrCqaSGTMyyqNt2H)
    - [ ] [(可選) 谷歌開發者: GZIP 還差遠了呢!](https://www.youtube.com/watch?v=whGwm0Lky2s)

- ### 網絡 (視頻)
    - [ ] [可汗學院](https://www.khanacademy.org/computing/computer-science/internet-intro)
    - [ ] [網絡傳輸協議中的數據壓縮](https://www.youtube.com/watch?v=Vdc8TCESIg8)
    - [ ] [TCP/IP 和 OSI 模型解析!](https://www.youtube.com/watch?v=e5DEVa9eSN0)
    - [ ] [TCP/IP 教程：傳輸數據包.](https://www.youtube.com/watch?v=nomyRJehhnM)
    - [ ] [HTTP](https://www.youtube.com/watch?v=WGJrLqtX7As)
    - [ ] [SSL 和 HTTPS](https://www.youtube.com/watch?v=S2iBR2ZlZf0)
    - [ ] [SSL/TLS](https://www.youtube.com/watch?v=Rp3iZUvXWlM)
    - [ ] [HTTP 2.0](https://www.youtube.com/watch?v=E9FxNzv1Tr8)
    - [ ] [視頻](https://www.youtube.com/playlist?list=PLEbnTDJUr_IegfoqO4iPnPYQui46QqT0j)
    - [ ] [子網絡解密 - 第五部分 經典內部域名指向 CIDR 標記](https://www.youtube.com/watch?v=t5xYI0jzOf4)

- ### 計算機安全
    - [MIT](https://www.youtube.com/playlist?list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [威脅模型：入門](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [控制攻擊](https://www.youtube.com/watch?v=6bwzNg5qQ0o&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=2)
        - [ ] [緩衝數據注入和防禦](https://www.youtube.com/watch?v=drQyrzRoRiA&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=3)
        - [ ] [優先權區分](https://www.youtube.com/watch?v=6SIJmoE9L9g&index=4&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [能力](https://www.youtube.com/watch?v=8VqTSY-11F4&index=5&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [在沙盒中運行原生代碼](https://www.youtube.com/watch?v=VEV74hwASeU&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=6)
        - [ ] [網絡安全模型](https://www.youtube.com/watch?v=chkFBigodIw&index=7&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [網絡安全應用](https://www.youtube.com/watch?v=EBQIGy1ROLY&index=8&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [標誌化執行](https://www.youtube.com/watch?v=yRVZPvHYHzw&index=9&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [網絡安全](https://www.youtube.com/watch?v=SIEVvk3NVuk&index=11&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [網絡協議](https://www.youtube.com/watch?v=QOtA76ga_fY&index=12&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [旁路攻擊](https://www.youtube.com/watch?v=PuVMkSEcPiI&index=15&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

- ### 釋放緩存
    - [ ] [Java 釋放緩存; 片段化數據 (視頻)](https://www.youtube.com/watch?v=StdfeXaKGEc&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=25)
    - [ ] [編譯器 (視頻)](https://www.youtube.com/playlist?list=PLO9y7hOkmmSGTy5z6HZ-W4k2y8WXF7Bff)
    - [ ] [Python 釋放緩存 (視頻)](https://www.youtube.com/watch?v=iHVs_HkjdmI)
    - [ ] [深度解析：論釋放緩存在 JAVA 中的重要性](https://www.infoq.com/presentations/garbage-collection-benefits)
    - [ ] [深度解析：論釋放緩存在 Python 中的重要性(視頻)](https://www.youtube.com/watch?v=P-8Z0-MhdQs&list=PLdzf4Clw0VbOEWOS_sLhT_9zaiQDrS5AR&index=3)

- ### 並行/並發編程
    - [ ] [Coursera (Scala)](https://www.coursera.org/learn/parprog1/home/week/1)
    - [ ] [論並行/並發編程如何提高 Python 執行效率 (視頻)](https://www.youtube.com/watch?v=uY85GkaYzBk)

- ### 設計模式
    - [ ] [UML統一建模語言概覽 (視頻)](https://www.youtube.com/watch?v=3cmzqZzwNDM&list=PLGLfVvz_LVvQ5G-LdJ8RLqe-ndo7QITYc&index=3)
    - [ ] 主要有如下的設計模式:
        - [ ] s(strategy)
        - [ ] singleton
        - [ ] adapter
        - [ ] prototype
        - [ ] decorator
        - [ ] visitor
        - [ ] factory, abstract factory
        - [ ] facade
        - [ ] observer
        - [ ] proxy
        - [ ] delegate
        - [ ] command
        - [ ] state
        - [ ] memento
        - [ ] iterator
        - [ ] composite
        - [ ] flyweight
    - [ ] [第六章 (第 1 部分 ) - 設計模式 (視頻)](https://youtu.be/LAP2A80Ajrg?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO&t=3344)
    - [ ] [第六章(第2 部分) - Abstraction-Occurrence, General Hierarchy, Player-Role, Singleton, Observer, Delegation (視頻)](https://www.youtube.com/watch?v=U8- PGsjvZc4&index=12&list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)
    - [ ] [第六章(第3 部分) - Adapter, Facade, Immutable, Read-Only Interface, Proxy (video)](https://www.youtube.com/watch?v=7sduBHuex4c&index=13&list=PLJ9pm_Rc9HesnkwKlal_buSIHA- jTZMpO)
    - [ ] [視頻](https://www.youtube.com/playlist?list=PLF206E906175C7E07)
    - [ ] [Head First 設計模型](https://www.amazon.com/Head-First-Design-Patterns-Freeman/dp/0596007124)
        - 儘管這本書叫做設計模式：重複使用模塊，但是我還是認為Head First是對於新手來說很不錯的書。
    - [ ] [基於實際操作對於入門開發者的建議](https://sourcemaking.com/design-patterns-and-tips)

- ### 信息傳輸, 序列化,和隊列化的系統
    - [ ] [Thrift](https://thrift.apache.org/)
        - [教程](http://thrift-tutorial.readthedocs.io/en/latest/intro.html)
    - [ ] [協議緩衝](https://developers.google.com/protocol-buffers/)
        - [教程](https://developers.google.com/protocol-buffers/docs/tutorials)
    - [ ] [gRPC](http://www.grpc.io/)
        - [gRPC 對於JAVA開發者的入門教程（視頻）](https://www.youtube.com/watch?v=5tmPvSe7xXQ&list=PLcTqM9n_dieN0k1nSeN36Z_ppKnvMJoly&index=1)
    - [ ] [Redis](http://redis.io/)
        - [教程](http://try.redis.io/)
    - [ ] [Amazon的 SQS 系統 (隊列)](https://aws.amazon.com/sqs/)
    - [ ] [Amazon的 SNS 系統 (pub-sub)](https://aws.amazon.com/sns/)
    - [ ] [RabbitMQ](https://www.rabbitmq.com/)
        - [入門教程](https://www.rabbitmq.com/getstarted.html)
    - [ ] [Celery](http://www.celeryproject.org/)
        - [Celery入門](http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html)
    - [ ] [ZeroMQ](http://zeromq.org/)
        - [入門教程](http://zeromq.org/intro:read-the-manual)
    - [ ] [ActiveMQ](http://activemq.apache.org/)
    - [ ] [Kafka](http://kafka.apache.org/documentation.html#introduction)
    - [ ] [MessagePack](http://msgpack.org/index.html)
    - [ ] [Avro](https://avro.apache.org/)

- ### 快速傅里葉變換
    - [ ] [什麼是傅立葉變換？論傅立葉變換的用途](http://www.askamathematician.com/2012/09/q-what-is-a-fourier-transform-what-is-it-used-for/)
    - [ ] [什麼是傅立葉變換？ (視頻)](https://www.youtube.com/watch?v=Xxut2PN-V8Q)
    - [ ] [關於 FFT 的不同觀點 (視頻)](https://www.youtube.com/watch?v=iTMn0Kt18tg&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=4)
    - [ ] [FTT 是什麼](http://jakevdp.github.io/blog/2013/08/28/understanding-the-fft/)

- ### 布隆過濾器
    - 給一個布隆過濾器m比特和k個哈希函數，所有的注入和相關測試都會是通過。
    - [布隆過濾器](https://www.youtube.com/watch?v=-SuTGoFYjZs)
    - [布隆過濾器 | 數據挖掘 | Stanford University](https://www.youtube.com/watch?v=qBTdukbzc78)
    - [教程](http://billmill.org/bloomfilter-tutorial/)
    - [如何寫一個布隆過濾器應用](http://blog.michaelschmatz.com/2016/04/11/how-to-write-a-bloom-filter-cpp/)

- ### van Emde Boas 樹
    - [ ] [爭論: van Emde Boas 樹 (視頻)](https://www.youtube.com/watch?v=hmReJCupbNU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=6)
    - [ ] [MIT課堂筆記](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-046j-design-and-analysis-of-algorithms-spring-2012/lecture -notes/MIT6_046JS12_lec15.pdf)

- ### 更深入的數據結構
    - [ ] [CS 61B 第 39 課: 更深入的數據結構](https://youtu.be/zksIj9O8_jc?list=PL4BBB74C7D2A1049C&t=950)

- ### 跳表
    - "有一種非常迷幻的數據類型" - Skiena
    - [ ] [隨機化: 跳表 (視頻)](https://www.youtube.com/watch?v=2g9OSRKJuzM&index=10&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [更生動詳細的解釋](https://en.wikipedia.org/wiki/Skip_list)

- ### 網絡流
    - [ ] [5分鐘簡析Ford-Fulkerson (視頻)](https://www.youtube.com/watch?v=v1VgJmkEJW0)
    - [ ] [Ford-Fulkerson 算法 (視頻)](https://www.youtube.com/watch?v=v1VgJmkEJW0)
    - [ ] [網絡流 (視頻)](https://www.youtube.com/watch?v=2vhN4Ice5jI)

- ### 不相交集 & 聯合查找
    - [ ] [不相交集](https://en.wikipedia.org/wiki/Disjoint-set_data_structure)
    - [ ] [UCB 61B - 不相交集; 排序 & 選擇(視頻)](https://www.youtube.com/watch?v=MAEGXTwmUsI&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=21)
    - [ ] Coursera (not needed since the above video explains it great):
        - [ ] [概覽](https://www.coursera.org/learn/data-structures/lecture/JssSY/overview)
        - [ ] [初級實踐](https://www.coursera.org/learn/data-structures/lecture/EM5D0/naive-implementations)
        - [ ] [樹狀結構](https://www.coursera.org/learn/data-structures/lecture/Mxu0w/trees)
        - [ ] [合併樹狀結構](https://www.coursera.org/learn/data-structures/lecture/qb4c2/union-by-rank)
        - [ ] [路徑壓縮](https://www.coursera.org/learn/data-structures/lecture/Q9CVI/path-compression)
        - [ ] [分析選項](https://www.coursera.org/learn/data-structures/lecture/GQQLN/analysis-optional)

- ### 快速處理數學
    - [ ] [整數運算, Karatsuba 乘法 (視頻)](https://www.youtube.com/watch?v=eCaXlAaN2uE&index=11&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [中國剩餘定理 (在密碼學中的使用) (視頻)](https://www.youtube.com/watch?v=ru7mWZJlRQg)

- ### 樹堆 (Treap)
    - 一個二叉搜索樹和一個堆的組合
    - [ ] [樹堆](https://en.wikipedia.org/wiki/Treap)
    - [ ] [數據結構：樹堆的講解(video)](https://www.youtube.com/watch?v=6podLUYinH8)
    - [ ] [集合操作的應用(Applications in set operations)](https://www.cs.cmu.edu/~scandal/papers/treaps-spaa98.pdf)

- ### 線性規劃（Linear Programming）（視頻）
    - [ ] [線性規劃](https://www.youtube.com/watch?v=M4K6HYLHREQ)
    - [ ] [尋找最小成本](https://www.youtube.com/watch?v=2ACJ9ewUC6U)
    - [ ] [尋找最大值](https://www.youtube.com/watch?v=8AA_81xI3ik)

- ### 幾何：凸包（Geometry, Convex hull）（視頻）
    - [ ] [Graph Alg. IV: 幾何算法介紹 - 第 9 課](https://youtu.be/XIAQRlNkJAw?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3164)
    - [ ] [Graham & Jarvis: 幾何算法 - 第 10 課](https://www.youtube.com/watch?v=J5aJEcOr6Eo&index=10&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [Divide & Conquer: 凸包, 中值查找](https://www.youtube.com/watch?v=EzeYI7p9MjU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=2)

- ### 離散數學
    - 查看下面的視頻：(這裡沒看到視頻= =）

- ### 機器學習（Machine Learning）
    - [ ] 為什麼學習機器學習？
        - [ ] [谷歌如何將自己改造成一家「機器學習優先」公司？ ](https://backchannel.com/how-google-is-remaking-itself-as-a-machine-learning-first-company-ada63defcb70)
        - [ ] [智能計算機系統的大規模深度學習 (視頻)](https://www.youtube.com/watch?v=QSaZGT4-6EY)
        - [ ] [Peter Norvig：深度學習和理解與軟件工程和驗證的對比](https://www.youtube.com/watch?v=X769cyzBNVw)
    - [ ] [谷歌云機器學習工具（視頻）](https://www.youtube.com/watch?v=Ja2hxBAwG_0)
    - [ ] [谷歌開發者機器學習清單 (Scikit Learn 和 Tensorflow) (視頻)](https://www.youtube.com/playlist?list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal)
    - [ ] [Tensorflow (視頻)](https://www.youtube.com/watch?v=oZikw5k_2FM)
    - [ ] [Tensorflow 教程](https://www.tensorflow.org/versions/r0.11/tutorials/index.html)
    - [ ] [Python 實現神經網絡實例教程（使用 Theano）](http://www.analyticsvidhya.com/blog/2016/04/neural-networks-python-theano/)
    - 課程:
        - [ ] [很棒的初級課程：機器學習](https://www.coursera.org/learn/machine-learning)
            - [視頻教程](https://www.youtube.com/playlist?list=PLZ9qNFMHZ-A4rycgrgOYma6zxF4BZGGPW)
            - 看第 12-18 集複習線性代數（第 14 集和第 15 集是重複的）
        - [ ] [機器學習中的神經網絡](https://www.coursera.org/learn/neural-networks)
        - [ ] [Google 深度學習微學位](https://www.udacity.com/course/deep-learning--ud730)
        - [ ] [Google/Kaggle 機器學習工程師微學位](https://www.udacity.com/course/machine-learning-engineer-nanodegree-by-google--nd009)
        - [ ] [無人駕駛工程師微學位](https://www.udacity.com/drive)
        - [ ] [Metis 在線課程 (兩個月 99 美元)](http://www.thisismetis.com/explore-data-science)
    - 資源:
        - 書籍: Data Science from Scratch: First Principles with Python: https://www.amazon.com/Data-Science-Scratch-Principles-Python/dp/149190142X
        - 網站: Data School: http://www.dataschool.io/

- ### Go 語言
    - [ ] 視頻:
        - [ ] [為什麼學習 Go 語言？ ](https://www.youtube.com/watch?v=FTl0tl9BGdc)
        - [ ] [Go 語言編程](https://www.youtube.com/watch?v=CF9S4QZuV30)
        - [ ] [Go 語言之旅](https://www.youtube.com/watch?v=ytEkHepK08c)
    - [ ] 書籍:
        - [ ] [Go 語言編程入門 (免費在線閱讀)](https://www.golang-book.com/books/intro)
        - [ ] [Go 語言聖經 (Donovan & Kernighan)](https://www.amazon.com/Programming-Language-Addison-Wesley-Professional-Computing/dp/0134190440)
    - [ ] [Go 語言新手訓練營](https://www.golang-book.com/guides/bootcamp)

--

## 一些主題的額外內容

    我為前面提到的某些主題增加了一些額外的內容，之所以沒有直接添加到前面，是因為這樣很容易導致某個主題內容過多。畢竟你想在本世紀找到一份工作，對吧？

- [ ] **動態規劃的更多內容** (視頻)
    - [ ] [6.006: 動態規劃 I: 斐波那契數列, 最短路徑](https://www.youtube.com/watch?v=OQ5jsbhAv_M&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=19)
    - [ ] [6.006: 動態規劃 II: 文本匹配, 二十一點/黑傑克](https://www.youtube.com/watch?v=ENyox7kNKeY&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=20)
    - [ ] [6.006: 動態規劃 III: 最優加括號方式, 最小編輯距離, 背包問題](https://www.youtube.com/watch?v=ocZMDMZwhCY&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=21)
    - [ ] [6.006: 動態規劃 IV: 吉他指法，拓撲，超級馬里奧.](https://www.youtube.com/watch?v=tp4_UXaVyx8&index=22&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.046: 動態規劃: 動態規劃進階](https://www.youtube.com/watch?v=Tw1k46ywN6E&index=14&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [6.046: 動態規劃: 所有點對最短路徑](https://www.youtube.com/watch?v=NzgFUwOaoIw&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=15)
    - [ ] [6.046: 動態規劃: 更多示例](https://www.youtube.com/watch?v=krZI60lKPek&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=12)

- [ ] **圖形處理進階** (視頻)
    - [ ] [異步分佈式算法: 對稱性破缺，最小生成樹](https://www.youtube.com/watch?v=mUBmcbbJNf4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=27)
    - [ ] [異步分佈式算法: 最小生成樹](https://www.youtube.com/watch?v=kQ-UQAzcnzA&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=28)

- [ ] MIT **概率論** (mathy, and go slowly, which is good for mathy things) (視頻):
    - [ ] [MIT 6.042J - 概率論概述](https://www.youtube.com/watch?v=SmFwFdESMHI&index=18&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 條件概率 Probability](https://www.youtube.com/watch?v=E6FbvM-FGZ8&index=19&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 獨立](https://www.youtube.com/watch?v=l1BCv3qqW4A&index=20&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 隨機變量](https://www.youtube.com/watch?v=MOfhhFaQdjw&list=PLB7540DEDD482705B&index=21)
    - [ ] [MIT 6.042J - 期望 I](https://www.youtube.com/watch?v=gGlMSe7uEkA&index=22&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 期望 II](https://www.youtube.com/watch?v=oI9fMUqgfxY&index=23&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 大偏差](https://www.youtube.com/watch?v=q4mwO2qS2z4&index=24&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 隨機遊走](https://www.youtube.com/watch?v=56iFMY8QW2k&list=PLB7540DEDD482705B&index=25)

- [ ] [Simonson: 近似算法 (視頻)](https://www.youtube.com/watch?v=oDniZCmNmNw&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=19)

## 視頻系列

 坐下來享受一下吧。 "netflix and skill" :P

- [ ] [個人的動態規劃問題列表 (都是短視頻喲)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)

- [ ] [x86 架構，彙編，應用程序 (11 個視頻)](https://www.youtube.com/playlist?list=PL038BE01D3BAEFDB0)

- [ ] [MIT 18.06 線性代數，2005 年春季 (35 個視頻)](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)

- [ ] [絕妙的 MIT 微積分：單變量微積分](https://www.youtube.com/playlist?list=PL3B08AE665AB9002A)

- [ ] [計算機科學 70, 001 - 2015 年春季 - 離散數學和概率理論](https://www.youtube.com/playlist?list=PL-XXv-cvA_iD8wQm8U0gG_Z1uHjImKXFy)

- [ ] [離散數學 (19 個視頻)](https://www.youtube.com/playlist?list=PL3o9D4Dl2FJ9q0_gtFXPh_H4POI5dK0yG)

- [ ] CSE373 - 算法分析 (25 個視頻)
    - [Skiena 的算法設計手冊講座](https://www.youtube.com/watch?v=ZFjhkohHdAA&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=1)

- [ ] [UC Berkeley 61B (2014 年春季): 數據結構 (25 個視頻)](https://www.youtube.com/watch?v=mFPmKGIrQs4&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)

- [ ] [UC Berkeley 61B (2006 年秋季): 數據結構 (39 個視頻)]( https://www.youtube.com/playlist?list=PL4BBB74C7D2A1049C)

- [ ] [UC Berkeley 61C: 計算機結構 (26 個視頻)](https://www.youtube.com/watch?v=gJJeUFyuvvg&list=PL-XXv-cvA_iCl2-D-FS5mk0jFF6cYSJs_)

- [ ] [OOSE: 使用 UML 和 Java 進行軟件開發 (21 個視頻)](https://www.youtube.com/playlist?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)

- [ ] [UC Berkeley CS 152: 計算機結構和工程 (20 個視頻)](https://www.youtube.com/watch?v=UH0QYvtP7Rk&index=20&list=PLkFD6_40KJIwEiwQx1dACXwh-2Fuo32qr)

- [ ] [MIT 6.004: 計算結構 (49 視頻)](https://www.youtube.com/playlist?list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-)

- [ ] [卡內基梅隆大學 - 計算機架構講座 (39 個視頻)](https://www.youtube.com/playlist?list=PL5PHm2jkkXmi5CxxI7b3JCL1TWybTDtKq)

- [ ] [MIT 6.006: 算法介紹 (47 個視頻)](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&nohtml5=False)

- [ ] [MIT 6.033: 計算機系統工程 (22 個視頻)](https://www.youtube.com/watch?v=zm2VP0kHl1M&list=PL6535748F59DCA484)

- [ ] [MIT 6.034 人工智能, 2010 年秋季 (30 個視頻)](https://www.youtube.com/playlist?list=PLUl4u3cNGP63gFHB6xb-kVBiQHYe_4hSi)

- [ ] [MIT 6.042J: 計算機科學數學, 2010 年秋季 (25 個視頻)](https://www.youtube.com/watch?v=L3LMbpZIKhQ&list=PLB7540DEDD482705B)

- [ ] [MIT 6.046: 算法設計與分析 (34 個視頻)](https://www.youtube.com/watch?v=2P-yW7LQr08&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

- [ ] [MIT 6.050J: 信息和熵, 2008 年春季 (19 個視頻)](https://www.youtube.com/watch?v=phxsQrZQupo&list=PL_2Bwul6T-A7OldmhGODImZL8KEVE38X7)

- [ ] [MIT 6.851: 高等數據結構 (22 個視頻)](https://www.youtube.com/watch?v=T0yzrZL1py0&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=1)

- [ ] [MIT 6.854: 高等算法, 2016 年春季 (24 個視頻)](https://www.youtube.com/playlist?list=PL6ogFv-ieghdoGKGg2Bik3Gl1glBTEu8c)

- [ ] [MIT 6.858計算機系統安全, 2014 年秋季](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

- [ ] 斯坦福: 編程範例 (17 個視頻)
    - [C 和 C++ 課程](https://www.youtube.com/watch?v=jTSvthW34GU&list=PLC0B8B318B7394B6F&nohtml5=False)

- [ ] [密碼學導論](https://www.youtube.com/watch?v=2aHkqB2-46k&feature=youtu.be)
    - [本系列更多內容 (不分先後順序)](https://www.youtube.com/channel/UC1usFRN4LCMcfIV7UjHNuQg)

- [ ] [大數據 - 斯坦福大學 (94 個視頻)](https://www.youtube.com/playlist?list=PLLssT5z_DsK9JDLcT8T62VtzwyW9LNepV)

## 計算機科學課程

- [ 在線 CS 課程目錄 ](https://github.com/open-source-society/computer-science)
- [CS 課程目錄 (一些是在線講座)](https://github.com/prakhar1989/awesome-courses)