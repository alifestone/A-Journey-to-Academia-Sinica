# 介紹
[Lehome Challenge 2026](https://lehome-challenge.com/) 是一場機械手臂摺衣服比賽。<br>
共分成兩個階段，第一階段將在 Isaac Sim 中訓練並評估機械手臂去摺衣服，第二階段將會實際運用到實體。
- 官方 Repo：https://github.com/lehome-official/lehome-challenge
- 我的 Repo：https://github.com/alifestone/lehome-challenge_S.N.N
# My Journey
這次非常有幸和 IDLab 的 [@KunHsiang](https://github.com/KunHsiang) 一起組隊（lehome-challenge_S.N.N）參與該比賽。<br>
以下將分享整個比賽的參與過程。
## Baseline 終於跑來了!!!!
一開始，老師和我們說 Baseline 要趕快跑起來。聽到這的我，「什麼是 Baseline？Baseline 可以吃嗎？」。<br>
現在回顧當時，老師的話固然是有其道理的。只有當 Baseline 跑出來才能進行下一階段的 improvement 或是對於不足的地方收集更多資料去 fine-tune。<br>
只不過，因為我是第一次碰這個東西，所以一些基礎的 setup 像找到相符的 Pytorch 版本（猜測是因為實驗室所使用的 5090 太新所致）、simulation 要求使用畫面，但實驗室的 server 是 headless 的 ...... 等一堆問題都成為我們團隊駐足不前的原因。<br>
其中最有趣的是一開始因為一些依賴包的版本不對導致 smolVLA 和 dp 的 success rate 一直是 0；act 更好笑，運氣好可以跑出個 56%，運氣不好也是 0%。<br>
印象深刻的是我們去檢查 simulation 的錄製畫面發現"機械手臂根本沒有動"!!!<br>
而這些問題隨著一行指令 (`uv pip install torch==2.11.0+cu128 torchvision==0.26.0+cu128 --index-url https://download.pytorch.org/whl/cu128 --index-strategy unsafe-best-match`) 全部被解決，也是令人哭笑不得。<br><br>
Baseline 跑出來的時間是 [3 月多](https://www.linkedin.com/posts/1ifestone_finally-finally-it-works-i-ugcPost-7438532951040225280-cJDP/?utm_source=share&utm_medium=member_desktop&rcm=ACoAAE5PCkMBl_9hhbIyeiFFLcBxvL_qZE1p2fc)，而比賽截止日是 4/20 ......
