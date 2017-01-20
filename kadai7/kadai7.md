# 課題7 レポート
 
## 課題  
 ダイナミックレンジの拡大  
 画素のダイナミックレンジを０から２５５にせよ.  
 下記はサンプルプログラムである.  
 課題作成にあたっては「Lenna」以外の画像を用いよ.  
 
 
標準画像「7.jpg」を原画像とする．この画像は縦2374画像，横1773画素による正方形のディジタルカラー画像である．

### プラグラム  
 ORG = imread('7.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
   **図1に示す．**  
   
pause;  
imhist(ORG); % 濃度ヒストグラムを生成、表示  
pause;  
   **図2に示す．**  
   
ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause; 

   **図3に示す．** 
   
ORG = uint8(ORG); % この行について考察せよ  
imhist(ORG); % 濃度ヒストグラムを生成、表示  
ORG=imread('7.png'); % 原画像の入力    
imagesc(ORG); axis image; % 画像の表示  
   **図4に示す．** 


以上のコマンドによって，原画像を読み込み，濃度ヒストグラムを表示する．  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/7.jpg)  
図0 原画像

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-0.png)  
図1 白黒濃淡画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-1.png)  
図2 濃度ヒストグラム

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-2.png)  
図3  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai7/kadai7-3.png)  
図4

## 考察  
 ORG = uint8(ORG);について考察する．  
 
 
