# 課題3レポート

標準画像「radio.jpg」を原画像とする．この画像は縦266画像，横400画素による長方形のディジタルカラー画像である．

ORG=imread('radio.jpg'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

以上のコマンドにより、表示した結果を図１に示す．

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai3_1.jpg)  
 　　　　　　　　　　　　　　　　　　　図1 原画像

次に、以下のコマンドを用いて輝度値が64以上の画素を1，その他を0に閾値処理したものを図2に示す。
IMG = ORG > 64; % 輝度値が64以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai3_2.jpg)  
図2 閾値処理１

次に、以下のコマンドを用いて輝度値が96以上の画素を1，その他を0に閾値処理したものを図2に示す。
IMG = ORG > 96; % 輝度値が96以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai3_3.jpg)  
図3 閾値処理2

次に、以下のコマンドを用いて輝度値が128以上の画素を1，その他を0に閾値処理したものを図2に示す。
IMG = ORG > 128; % 輝度値が128以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai3_4.jpg)  
図4 閾値処理3

次に、以下のコマンドを用いて輝度値が192以上の画素を1，その他を0に閾値処理したものを図2に示す。
IMG = ORG > 192; % 輝度値が192以上の画素を1，その他を0に変換
imagesc(IMG); colormap(gray); colorbar;

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai3_5.jpg)  
図5 閾値処理4
