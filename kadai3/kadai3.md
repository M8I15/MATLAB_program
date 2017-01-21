# 課題3 レポート  


## 課題  
課題３　閾値処理  
% 閾値を4パターン設定し,閾値処理た画像を示せ．  
% 課題作成にあたっては「Lenna」以外の画像を用いよ．  
標準画像「3-1.jpg」を原画像とする．この画像は縦4000画像，横3000画素による正方形のディジタルカラー画像である.　　

### プログラムソース  
clear; % 変数のオールクリア  

ORG=imread('3-1.png'); % 原画像の入力  
**図0に示す**  

ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
**図1に示す**  

IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換  
imagesc(IMG); colormap(gray); colorbar;  
pause;  
**図2に示す**  

IMG = ORG > 96;  
imagesc(IMG); colormap(gray); colorbar;  
pause;  
**図3に示す**  

IMG = ORG > 128;  
imagesc(IMG); colormap(gray); colorbar;  
pause;  
**図4に示す**  

IMG = ORG > 192;  
imagesc(IMG); colormap(gray); colorbar;  
**図5に示す**  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai3/3.jpg)  
図0 原画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai3/kadai3-0.png)  
図1 白黒濃淡画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai3/kadai3-1.png)    
図2 輝度値64  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai3/kadai3-2.png)  
図3 輝度値96  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai3/kadai3-3.png)  
図4 輝度値128

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai3/kadai3-4.png)  
図5 輝度値192  

### 考察  
輝度値が大きくなるにつれ黒くなるっ分が増えていることが分かった．  
