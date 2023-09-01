---
title: 趨勢介紹
description: 
categories:
 - 統計觀念
date: 2023-04-01 14:25
tags: [數據建模]
thumbnail: https://raw.githubusercontent.com/meiyulee/pic001/master/AIecon/free14letecture_60.JPG
---

## 前言

數字趨勢是日常很常見的字眼。不過對「趨勢」這一詞被用到很浮濫，特別是在時間為橫軸的圖形上特別明顯。

為什麼時間軸上的數字會讓多數人使用上「趨勢」一詞，認為他們在做趨勢分析呢？

原因在於任何數字被打在時間軸上，再以Excel或圖像視覺化的折線圖表示時就讓人類的視覺發生「趨勢感」。你會感覺從左到又有一個趨勢出現。例如左低右高，即使數字在其中上上下下，你也會感覺有上升趨勢。

重點就在圖像中的左右邊的數字位置！

你在看任何折線圖時只要圖像能顯像的左右邊數字位置有高低差發生，就會讓人類感覺好像有個上升或下降的感覺。這是人類最為習慣且不自覺使用上的「**兩點比較法**」，或稱為「**高低差比較法**」！

因人類非常習慣且不自覺地使用，在圖像上就形成視覺的錯覺，以為數字點圖有趨勢！事實並沒有！

## 直線未必是趨勢

在還沒有小學，孩子們在玩兩點連連看時，就是兩點可以連成一直線。到了高中，兩點連成的直線出現在二維空間內形成直線方程式。但這也只是兩點連成的直線，沒有趨勢特性，所以不是趨勢。

在高中除了在二維空間內可以點出兩點的數對位置，將之連線，並計算出直線方程式，連線上的各點皆是存在。不過，現實的數字的兩點，未必表示這兩點的連線上有點存在。例如，每日台積電的收盤價，我們將之在有時間軸的二維空間上點出來後，這兩點中間是沒有任何記錄的。

此時你將這兩點用直線連在一起，就代表這兩點中間的直線上都是有記錄。和前述的實際記錄是矛盾的。也就是說，單純的兩點連成一直線方式在現實的記錄方式上是不成立的。

那這樣的兩點連成直線就是趨勢嗎？答案不是。

既然我們可以任兩點連出一條直線，你認為這樣的一直線能夠給你趨勢訊號是種錯覺。因為間隔的兩點連線，也就是如折線一樣，一下往上，一下往下。那這算趨勢嗎？當然不是。所以兩點連線並不能產生趨勢。

## 時間造成趨勢錯覺

為何在有時間軸的二維空間上，以兩點連成一直線方式能讓你感覺有趨勢？原因在於人類過往受過的訓練以及時間軸的由左到右，讓人覺得有趨勢產生。這是來自「向量」的訓練和從零開始由左到右的數字排序方式，讓我們感覺到趨勢出現。

## 趨勢定義

所謂的趨勢是指**超過兩點的數字數對**，以科學方式建立的數學式，再以圖形表現出來，形成趨勢圖。

我們需要提升兩點連成一直線的高中數學觀念，到達趨勢概念。所以此時不是兩點，而是超過兩點，由這些點形成趨勢。趨勢的表現方式可以是直線，也可以是非直線，例如拋物線、圓形、橢圓形、指數、log函數、三角函數等，當然也可以是超過直線和非直線形式的曲線(Curve)。通常曲線形式以微積分的泰勒展開式表現，也就是高次方的數學方程式。而泰勒展開式等式右邊的最後還會有一個誤差項。這個誤差項是做為控制整個泰勒展開式要精準到多少。只要愈精準，這個誤差就會愈小。


那如何為超過兩點的數字數對建立趨勢呢？一般有最小平方法或最大概似法等，其他的方法可以參考統計學的點估計。

## 迴歸分析找趨勢

雖然說迴歸分析可以找趨勢，但統計學的迴歸分析特別強調對誤差的三大假設 — 對誤差有分配假設、變異數同質和兩兩之間的數對沒有相關。如果從數學角度來看，也能使用最小平方法和最大概似法一樣找出估計式(以數學式方式呈現)。所以為了不創造新的方法名詞，這裡仍用「迴歸分析」代稱，但為了和統計學的迴歸分析做一區隔，將之稱為「傳統迴歸分析」或「傳統迴歸模型」。

另外，傳統迴歸分析或計量經濟學都將將模型設定為「直線」。這點非常重要，也是為何傳統迴歸分析和計量經濟學都不適用大數據和人工智慧的精準建模。所謂精準建模是需要符合數據規律而成的數學模型，而前述的兩種方法被設計以「直線」為主。不符合直線，那就是將數據轉換到有接近直線的特徵。也就是說，理論上以為發散，無法收斂的原數據，需要符合理論需要和假設，將數據轉啊轉，轉換成合適套用理論模型的格式。至於，轉換後的數據能不能再回到原數據，有的不是討論的重點就被忽略了。

迴歸分析法本身是針對特定的數字型數對，配適出滿足誤差最小原則/解釋力最大原則的數學式。那麼我們就得先設定好你要函數形式為何。傳統迴歸分析就是設定「直線」形式。當然，從數學角度則是各種的數學函數形式都是可選的。

為何傳統迴歸分析和我說的迴歸分析有此差異，原因在於傳統迴歸分析的使用是為了檢定迴歸係數的顯著性或了解差異。但這不是建模！也就是你的分析目標不同，自然就該選擇合適的分析方法。例如，我們想知道A和B的關聯性，那當然就是要看迴歸係數的大小和是否能被信任。但如果你已經將數字做了轉換，那就得做還原動作。

可問題是常見的統計套軟沒有這樣的功能，所以在這些應用研究中充滿了各種的人為干預和認定意識！如果用這樣的方法放在大數據和人工智慧上，那麼所謂的趨勢，真得好好思量。

即使你說現在有新的迴歸方法，如嶺迴歸、LASSO之類的。這類的迴歸看似自變數有其存在意義，卻也能看到調整方式是降低自變數的影響性，轉為截距和誤差項的重要性。再運用一些演算法的方式，例如數字可以有樣本平均數、變異數等係數，以此為起始點，對數字的數對做等差切割，讓電腦運算各種可能，只要能做到降低誤差到無法再降，那就表示在該數字數對下已經估計到不能再精準了。我們就能將之視為「預測值」。同樣的方法反覆K次，K至少1000次以上，已計算出Accurancy值。產出就是圖和Accurancy值。

這樣的作法並沒有做到數據建模。你以為有圖就表示有做到數據建模，實際不然。所以想學大數據分析，想用電腦程式或軟體幫助你跑大數據分析都要注意有沒有數據的數學式；如果數據有轉換就要還原，再看還原後的模型為何。後者在統計學分析法上很難重新被驗證，因為當你還原回原數據的數學式後，也該為係數的統計量找出抽樣分配和檢定所需的臨界值。別以為你用轉換後的數據滿足傳統迴歸分析，或從此延伸出來的各種統計分析方法，還原數據後的數學模型檢驗也是需要的。

## 傳統迴歸分析的趨勢問題

由於傳統迴歸分析使用前，需要先人為設定，因此產生以下的問題：

1. 人為認定數據的起迄，非符合數據特性
2. 套用線性模型、轉成平方形式，或相減模式，以符合理論對數據的要求，非符合數據特性
3. 自變數選擇問題
4. 資料缺遺問題
5. 殘差處理以檢定為主，前提需要先知道分配。如果找不到分配，就用平均數應該會有的極限理論方式全都近似常態

因此，當使用者用傳統迴歸分析方法，為數據建立趨勢時，只能知道趨勢方向：上升、下降，以及趨勢力道：斜率絕對值。而想為數據建立趨勢，通常是以時間為自變數，於是衍生到最後，連建立趨勢都省略，直接用前述的折線圖表示，以觀察法看出趨勢方向就是趨勢。

甚至，變成以原數據轉換成技術指標，如移動平均，做原數據和移動平均值的大小比較，看出「趨勢」和「趨勢轉折」。此種兩點比較方式，如前所述，並沒有任何趨勢含義。兩點比較來自分類法。例如移動平均為基準，原數據的數字和其比較，形成「在其上」和「在其下」兩類別。支持這種做法的使用者的趨勢感，來自移動平均值的平滑化連線。這樣的連線仍有前述看似折線圖，其實是點圖。那兩點之間的線段上沒有任何意義。

為什麼會有這些不以原數據趨勢建立的方法，並以此成為主流呢？理由是，

1. 簡單好理解。沒有學歷限制，沒有知識限制，是人類的本能
2. 容易操作，只要會畫垂直線，做點對點的比對即可
3. 寫入電腦的演算法內相對於算迴歸還簡單
4. 只要會打出點圖，再用線段連線，就能看圖說故事

於是，傳統迴歸分析法就像神壇，所有人都以此說自己的數據來自於此，或自己解讀趨勢圖的經驗來自於此。事實是前述的四點簡單化、大眾化、主觀化的理由，和傳統迴歸分析能夠提供的趨勢資訊沒有想像中的多，導致看圖說故事成為現行主流。就連當初大數據方興未艾時，圖像視覺化是主流，多數人都認為這是大數據的重要產出。

可當大數據和人工智慧一起時，圖像產出只是結果，中間最為需要的「數據分析」方法和結果才是整個大數據和人工智慧被人接受和信任的可能。特別是中間過程的數據分析結果所需的「驗證」功能迄今仍未見到。現在的大數據和人工智慧都還是處於「主觀」，也就是網上有人提到的「AI訓練AI」而你不知道AI真偽的問題。

目前熱夯到不行的生成式AI，甚至被美國媒體認為將會主導未來十年的科技和科技應用，就是犯了上述的問題。只要沒有驗證功能就有問題。最近有項改良GPT的方式來自，訓練獎勵模型，以得分機制訓練資料，做到文字的精準度。看似很好，只要得分機制不是小數點後128位或更多，這些模型同樣無法控制誤差，也不會跟你說誤差多大，只會用accurancy的數字再次讓使用者相信這套GPT方法是可行且優異的。

## 改善傳統迴歸分析方法的重點

王冠先和李玫郁在2019年解決了傳統迴歸分析問題的第二點和第五點。第二點在2021年Hsiao等人的論文中進一步由AI決定最佳的模型形式。第五點則是Chan等人在2021年以論文形式展現分配對股市行為的表現特徵。王冠先和李玫郁在2015和2016年解決了第三點。同樣第三點也在PSCCC股份有限公司時期推出免費軟體中有提及，付費軟體中可使用。

但對於第一點在2021年以前始終沒有辦法解決。直到2023年Wang等人發行【Accurate New Stock Analytic Model】一書，17個數學模型的後三者從迴歸的基礎本質出發：為自變數和應變數建立解釋力最高的模型。迴歸本身選擇自變數時就是要選擇和應變數線性相關高的變數。於是，第一點被「多線段法」的迴歸模型解決了。

至於為何大家都沒想到這點呢？只能說是後來迴歸被濫用到不管你會不會統計學都能被套用進去，導致如財經和企管的各種迴歸模型應用，出現那些不符合迴歸要求的自變數選擇後造成很不理想的分析結果。甚至期刊主編都看不上眼，認為單一指標的分析都太低級，迴歸分析方法不夠複雜等，拒絕刊登這些創新型，可以為數據指標建立更良好的模型和即時性趨勢指標訊號的論文。

如果要和大數據和人工智慧接軌的傳統迴歸分析方法就該回到迴歸本質，而非為了使用者自己抓到的數據期間，然後一次性跑迴歸，用一條直線估計式就了事。大數據和人工智慧如果照著使用者或研究者這樣做，首先，這電腦運算前還得先寫個經驗學習模型，使其如專家學者一樣可以判斷數據期間。然而，專家學者們判斷的數據期間就真的準確嗎？數據反映說不定不是這回事！

那麼在多線段法的迴歸模型中，相比於傳統迴歸分析法，是哪點產生差異呢？答案是：

**內生化樣本數**！！

如果是要找趨勢，時間為自變數時，樣本數的排序就能對應上時間代號。如此一來，只要能在內化樣本數過程中，滿足趨勢的解釋力極大原則(此點可以成為AI的判斷原則)，就能解決第一點傳統迴歸分析的問題。

這和線性規劃概念很像。你需要有目標式、限制式，和極值原則。

* 所有的測試數字來自限制式，如同我們要內化的樣本數，依照時間排序一個一個加入
* 測試數字要放入目標式的數學式去計算。這如同我們要將樣本個數的每個數對都放入跑迴歸，得到估計式
* 極值原則是判斷法則，在線性規劃中，如果是要極大值，那麼目標式的數學式所得結果就要和前一個去比較，如果變大就保留，如果變小就停止。同樣，做迴歸時也是如此。

如此一來就解決第一點，同時也能在AI判斷後自動顯現數字本身告知的「趨勢轉折」，而非依靠原數字的數字轉換後(指的是移動平均)，和原數字做比較形成趨勢轉折。

另外做趨勢分析的人想知道的趨勢方向和力道更加精準，因為在檢測樣本數內化過程中，特定期間內的估計式滿足解釋力最大原則，而非全部的數據只跑一條估計式。

![](https://raw.githubusercontent.com/meiyulee/pic001/master/AIecon/free14letecture_60.JPG)