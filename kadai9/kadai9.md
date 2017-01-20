# 課題9 レポート  
 
 ## 課題  
 課題９ メディアンフィルタと先鋭化   
 メディアンフィルターを適用し，ノイズ除去を体験せよ.   
 各自，Lenna以外の画像を用いよ.  
 
標準画像「9」を原画像とする．この画像は縦2364画像，横1773画素による正方形のディジタルカラー画像である.  
 ### プログラムソース   
 
ORG = imread('9.jpg'); % 画像の読み込み  
ORG = rgb2gray(ORG); % 白黒濃淡画像に変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
 **図1に示す**  

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  
pause;  
 **図2に示す**   

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  
 **図3に示す**  
 
IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  
 **図4に示す**  
 
f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
pause;  
 **図5に示す**  
 

以上のプログラムソースを表示した結果を図1から5までに示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai9/9.jpg)  
図0 原画像

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai9/kadai9-0.png)  
図1 白黒濃淡画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai9/kadai9-1.png)  
図2 ノイズ添付  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai9/kadai9-2.png)  
図3 平滑化フィルタで雑音除去  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai9/kadai9-3.png)  
図4 メディアンフィルタで雑音除去  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai9/kadai9-4.png)  
図5 フィルタを設計  


 ## 考察  
 
 
