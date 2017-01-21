# 課題１レポート
 
## 課題  
 課題１　標本化間隔と空間解像度  
 画像をダウンサンプリングして（標本化間隔を大きくして）  
 表示せよ．  
 下記はサンプルプログラムである．  
 課題作成にあたっては「Lenna」以外の画像を用いよ．  
 
 標準画像「1」を原画像とする．この画像は縦512画像，横512画素による正方形のディジタルカラー画像である．
 （図0に示す）  
 
### プログラムソース  
 
 clear; % 変数のオールクリア  

ORG=imread('1.jpg'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示  
pause; % 一時停止  
**図1に示す**  

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大  
imagesc(IMG2); axis image; % 画像の表示  
pause; % 一時停止  
**図2に示す**

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,4,'box'); % 画像の拡大  
imagesc(IMG2); axis image; % 画像の表示  
pause; % 一時停止  
**図3に示す**

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,8,'box'); % 画像の拡大  
imagesc(IMG2); axis image; % 画像の表示  
pause; % 一時停止  
**図3に示す**  

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,16,'box'); % 画像の拡大  
imagesc(IMG2); axis image; % 画像の表示  
pause; % 一時停止  
**図4に示す**

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,32,'box'); % 画像の拡大  
imagesc(IMG2); axis image; % 画像の表示  
pause; % 一時停止  
**図5に示す**  

IMG = imresize(IMG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,64,'box'); % 画像の拡大  
imagesc(IMG2); axis image; % 画像の表示  
**図6に示す**  

以上のプログラムソースより，以下の図1から図6までの結果を表示  

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/1.jpg)  
図0 原画像

原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．

1/2サンプリングの結果を図２に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/kadai1-1.png)  
図1 1/2サンプリング

同様に原画像を1/4サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい

1/4サンプリングの結果を図３に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/kadai1-2.png)  
図2 1/4サンプリング．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/kadai1-3.png)  
図3 1/8サンプリング

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/kadai1-4.png)  
図4 1/16サンプリング

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/kadai1-5.png)  
図5 1/32サンプリング

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai1/kadai1-6.png)  
図6 1/64サンプリング

このようにサンプリング幅が大きくなると，モザイク状のサンプリングが発生するので原画像と比較すると見えずらくなることがわかる．
