# 課題5 レポート
 ## 判別分析法

標準画像「5」を原画像とする．この画像は縦2364画像，横1773画素によるディジタルカラー画像である．

ORG=imread('5.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

によって，原画像を読み込み，表示した結果を図1,2,3に示す．  

また，ソースコードは以下のようになる．  

H = imhist(ORG); %ヒストグラムのデータを列ベクトルEに格納  
myu_T = mean(H);  
max_val = 0;  
max_thres = 1;  
for i=1:255  
C1 = H(1:i); %ヒストグラムを2つのクラスに分ける  
C2 = H(i+1:256);  
n1 = sum(C1); %画素数の算出  
n2 = sum(C2);  
myu1 = mean(C1); %平均値の算出  
myu2 = mean(C2);  
sigma1 = var(C1); %分散の算出  
sigma2 = var(C2);  
sigma_w = (n1 *sigma1+n2*sigma2)/(n1+n2); %クラス内分散の算出  
sigma_B = (n1 *(myu1-myu_T)^2+n2*(myu2-myu_T)^2)/(n1+n2); %クラス間分散の算出  
if max_val<sigma_B/sigma_w  
max_val = sigma_B/sigma_w;  
max_thres =i;  
end;  
end;  

IMG = ORG > max_thres;  
imagesc(IMG); colormap(gray); colorbar;  


![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai5/5.jpg)  
図1 原画像

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai5/kadai5-0.png)  
図2　原画像（白黒）

![原画像](https://github.com/M8I15/MATLAB_program/blob/master/kadai5/kadai5-1.png)  
図3 判別分析法を用いた画像二値化
