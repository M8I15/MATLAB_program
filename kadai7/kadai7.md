# 課題7 レポート
 
﻿## 課題  
 ダイナミックレンジの拡大  
 画素のダイナミックレンジを０から２５５にせよ.  
 下記はサンプルプログラムである.  
 課題作成にあたっては「Lenna」以外の画像を用いよ.  
 
 
標準画像「7.jpg」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

﻿### プラグラム  
 ORG = imread('7.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
imhist(ORG); % 濃度ヒストグラムを生成、表示  
pause;  
ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  
ORG=imread('7.png'); % 原画像の入力    
imagesc(ORG); axis image; % 画像の表示  

によって，原画像を読み込み，表示した結果を図１に示す．  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/7.jpg)  
図1 原画像

原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

1/2サンプリングの結果を図２に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-0.png)  
図2 1/2サンプリング

同様に原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．すなわち，

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

とする．1/4サンプリングの結果を図３に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-1.png)  
図3 1/4サンプリング

1/8から1/32サンプリングは，

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大

を繰り返す．サンプリングの結果を図４～６に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-2.png)  
図4 1/8サンプリング

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-3.png)  
図5 1/16サンプリング
