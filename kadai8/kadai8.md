# 課題8 レポート  
 
 ## 課題 ラベリング  
二値化された画像の連結成分にラベルをつけよ．  
下記はサンプルプログラムである．   
課題作成にあたっては「Lenna」以外の画像を用いよ．   

標準画像「8」を原画像とする．この画像は縦2508画像，横1672画素による正方形のディジタルカラー画像である．  


### プログラム  

ORG = imread('8.jpg'); % 画像の読み込み   
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換    
imagesc(ORG); colormap(gray); colorbar; % 画像の表示    
pause　　
　　**図1に示す**　　
  
IMG = ORG > 128; % 閾値128で二値化   　
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  
　  **図2に示す**　　
   
IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  
pause;  
　　**図3に示す**  
  
 　　
![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai8/8.jpg)  
図0  原画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai8/kadai8-0.png)    
図1 白黒濃淡画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai8/kadai8-1.png)  
図2 閾値128で二値化   

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai8/kadai8-2.png)  
図3 


