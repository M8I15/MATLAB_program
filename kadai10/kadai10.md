# 課題10 レポート
## 画像のエッジ抽出
### 次のプログラムを参考にして，エッジ抽出を体験する．

標準画像「10」を原画像とする．

ORG=imread('10.jpg'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示


によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai10/kadai10-0.png)  
図1 原画像

原画像を1/2サンプリングするには，画像を1/2倍に縮小した後，2倍に拡大すればよい．なお，拡大する際には，単純補間するために「box」オプションを設定する．

IMG = imresize(ORG,0.5); % 画像の縮小  
IMG2 = imresize(IMG,2,'box'); % 画像の拡大



![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai10/kadai10-1.png)  
図2 

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai10/kadai10-2.png)  
図3 

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai10/kadai10-3.png)  
図4
