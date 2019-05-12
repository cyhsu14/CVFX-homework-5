# CVFX-homework-5
Homework 4 for CVFX, team 7.

### Multi-view images

### Image alignment results

### Generate the multi-view 3D visual effects

### Use PS to enhance effect

### Complete 3 different effects

#### Feature Extraction

#### Stop Motion

我們用上述圖片，沒有align的情況下直接做成gif。在拍照時，有用手機的格線有對水平線跟中心點的，所以直接製成gif時作為主角的樹理所當然的會為在旋轉軸上。

<img src="./assets/stopmo.gif" width="300px">

我們認為只要影像在拍攝的時候有讓主角位在影像中央、水平方向沒有變動、每張影像拍攝的位置和主角的距離一樣就可以直接製成gif，並且就會有Stop motion的效果。

雖然沒有用到feature extraction得到好的Stop motion，但因課程提供的範例都是使用camera matrix來完成的，所以我們認為我們的做法是符合要求的。

1. The Matrix：從影片(<a href="https://upload.wikimedia.org/wikipedia/en/transcoded/3/31/The_Matrix_Bullet_Time_Effect.ogv/The_Matrix_Bullet_Time_Effect.ogv.240p.vp9.webm">影片連結</a>)可以看出該畫面是讓演員站在攝影機們的中央拍攝的，所以推測在後處理時並沒有用alignment。
2. 跳起來：圖片來自一個提供photo booth租用的網站(<a href="https://www.limelightphotobooth.com/matrix-cam-180-bullet-time-photo-booth/">網站連結</a>)，根據網站的描述和圖片，3, 5, 7, 12, 24, 或 48台相機排列成一個在同一平面上的半圓並且會同時捕捉影像，推測也是不需要用alignment就可以直接製成gif。
3. 婚攝：圖片來自一個婚攝的blog(<a href="https://www.jlbwedding.com/the-seven-camera-rig/">網站連結</a>)，內文描述到該影像是用7台攝影機排成一排拍攝的，這也可以解釋為何該gif轉的幅度沒有第二張跳起來那張多，因為不是排成一個半圓環繞主角，而是一條緊密的直線。

若影像並沒有符合「主角位在影像中央、水平方向沒有變動、每張影像拍攝的位置和主角的距離一樣」的要求，我們認為feature extraction和alignment可以幫的只在於水平校正，雖然這次作業並沒有實作，我也還沒想清楚要怎麼做。

CamSwarm是一篇2015年的paper(<a href="https://arxiv.org/pdf/1507.01148.pdf">paper 連結</a>)，他們開發出了一款app可以透過wifi連接讓不同手機同時拍的照片可以合成有stop motion(內文使用bullet time)效果的gif。原理是透過手機得到拍照位置，然後用<a href="https://www.microsoft.com/en-us/research/wp-content/uploads/2016/07/Sinha-ICCV09.pdf">Piecewise Planar Stereo for Image-based Rendering</a>這個方法得到視角的內差。

說了這麼多，我只想論證在作業期限內我沒有想到除了讓照片品質好以外的方法做stop motion。

#### Live Photo
