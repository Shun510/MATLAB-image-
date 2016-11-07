﻿# 課題2レポート

標準画像「boby」を原画像とする．この画像は縦444画像，横469画素による長方形のディジタルカラー画像である．

ORG=imread('boby.png'); % 原画像の入力  
imagesc(ORG); axis image; % 画像の表示
colormap(gray);　%カラーをグレーにする
によって，原画像を読み込み，表示した結果を図１に示す．

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai2_1.png)  
図1 原画像

２階調画像の生成をするためには、

IMG = ORG>128;
imagesc(IMG); colormap(gray); colorbar;  axis image;

２階調画像の生成結果を図２に示す．

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai2_2.png)  
図2 ２階調画像

同様に原画像を４階調画像にするには，

IMG0 = ORG>64;
IMG1 = ORG>128;
IMG2 = ORG>192; 
IMG = IMG0 + IMG1 + IMG2;

とする．４階調画像の生成結果を図３に示す．

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai2_3.png)  
図3 4階調画像

８階調画像

IMG0 = ORG>32;
IMG1 = ORG>64;
IMG2 = ORG>128;
IMG3 = ORG>192;
IMG4 = ORG>224;
IMG5 = ORG>256;
IMG = IMG0 + IMG1 + IMG2 + IMG3 + IMG4 + IMG5;


![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai2_4.png)  
図4 8階調画像
