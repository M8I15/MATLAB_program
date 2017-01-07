# 課題5 レポート
 ## 判別分析法

標準画像「5」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．

ORG=imread('5.jpg'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai5/5.jpg)  
図1 原画像

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai5/kadai5-0.png)  
図2 


![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai5/kadai5-1.png)  
図3 
