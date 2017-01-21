# 課題2 レポート  
 
## 課題  
課題２　階調数と疑似輪郭  
２階調，４階調，８階調の画像を生成する．  
課題作成にあたっては「Lenna」以外の画像を用いよ．  

### プログラムソース  
clear; % 変数のオールクリア  

ORG=imread('2-1.png'); % 原画像の入力  
**図0に示す**  

ORG = rgb2gray(ORG); colormap(gray); colorbar;  
imagesc(ORG); axis image; % 画像の表示  
pause; % 一時停止  
**図1に示す**  

% ２階調画像の生成  
IMG = ORG>128;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  
pause;  
**図2に示す**  

% ４階調画像の生成  
IMG0 = ORG>64;  
IMG1 = ORG>128;  
IMG2 = ORG>192;  
IMG = IMG0 + IMG1 + IMG2;  
imagesc(IMG); colormap(gray); colorbar;  axis image;  
**図3に示す**  

% ８階調については，各自検討してください  ．

% ８階調画像の生成  
 IMG0 = ORG>32;    
 IMG1 = ORG>64;    
 IMG2 = ORG>96;    
 IMG3 = ORG>128;    
 IMG4 = ORG>160;   
 IMG5 = ORG>192;    
 IMG6 = ORG>224;    
 IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5 + IMG6;  
 imagesc(IMG); colormap(gray); colorbar;  axis image;    
 pause;   
**図4に示す**  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai2/2.png)  
図0 原画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai2/kadai2-0.png)  
図1 白黒画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai2/kadai2-1.png)  
図2 2階調

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai2/kadai2-2.png)  
図3 4階調

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai2/kadai2-3.png)  
図4 8階調

### 考察  
一つの画素に各色く記憶領域を割り当てると，2の1乗で2階調，2の2乗で4階調，2の3乗で8階調と表現できる．  
階調が増えるとともにbit数も大きくなるのでよりきめ細かく表現できる．  
