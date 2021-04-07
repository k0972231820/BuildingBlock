# BuildingBlock
# 偵測出影像中每個不同積木的內容與位置

![image](https://user-images.githubusercontent.com/8476048/111865197-88555b00-89a0-11eb-85b8-daf7b481e3a3.png)

<br>
<h3>BuildingBlock</h3>

首先將影像轉換成HSV的色彩空間，並將積木上特殊的顏色二值化成黑白影像

![image](https://user-images.githubusercontent.com/8476048/113868470-49b60200-97e2-11eb-97ae-03d8c6bed7ef.png)

<br>
並透過FindContours找出所有的積木

![image](https://user-images.githubusercontent.com/8476048/113869556-71f23080-97e3-11eb-9f23-a814f7d8bcf7.png)

<br>
接著利用透視轉換將取得的積木影像轉正，並與原始積木影像做每個pixel的比較，pixel相似度最高的即為我們要的結果
<br>
(每個找到的積木Contour都將旋轉4次90度並與原始積木影像做比較)

![image](https://user-images.githubusercontent.com/8476048/113870266-3c9a1280-97e4-11eb-9840-4401a098ec27.png)

最後將比較出的結果顯示在畫面上

![image](https://user-images.githubusercontent.com/8476048/113870721-b6320080-97e4-11eb-85c6-0d1e5df3cba1.png)
