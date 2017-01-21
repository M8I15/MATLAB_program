# 課題4 レポート  

## 課題  
 課題４　画像のヒストグラム  
 画素の濃度ヒストグラムを生成せよ．  
 課題作成にあたっては「Lenna」以外の画像を用いよ．  
 
標準画像「4.jpg」を原画像とする．この画像は縦4000画像，横3000画素による正方形のディジタルカラー画像である．

### プログラムソース  
clear; % 変数のオールクリア  

ORG=imread('4.png'); % 原画像の入力  
**図0に示す**  

ORG=rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar;  
pause;  
**図1に示す**  

imhist(ORG); % ヒストグラムの表示  
**図2に示す**  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai4/4.png)  
図0 原画像

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai4/kadai4-0.png)  
図1 白黒濃淡画像  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai4/kadai4-1.png)  
図2 ヒストグラムの表示  

### 考察  
　図から原画像の濃度値がどのくらいあるのか，暗いところ・明るいところ
 で，どのような結果がでるか分かった．
