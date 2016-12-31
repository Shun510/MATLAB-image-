# 課題7レポート

標準画像「radio.jpg」を原画像とする．この画像は縦266画像，横400画素による長方形のディジタルカラー画像である．

ORG=imread('radio.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

以上のコマンドにより、原画像を白黒濃淡画像へ変換した結果を図１に示す．    

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai7_1.jpg)  
図1 原画像

次に、以下のコマンドを用いて濃度ヒストグラムを生成し表示した結果を、図２に示す  

imhist(ORG); % 濃度ヒストグラムを生成、表示 

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai7_2.jpg)  
図2　 濃度ヒストグラム

以下のコマンドを用いて、カラーマップの全範囲の色を使用するイメージとして表示した結果を図３に示す。

ORG = double(ORG);  
mn = min(ORG(:)); % 濃度値の最小値を算出  
mx = max(ORG(:)); % 濃度値の最大値を算出  
ORG = (ORG-mn)/(mx-mn)*255;  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  


![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai7_3.jpg)  
図３　スケーリングした色によるイメージの表示


スケーリングした原画像をクラス uint8 の符号なし 8 ビット (1 バイト) 整数に変換した結果を図４に示す。


ORG = uint8(ORG);   
imhist(ORG); % 濃度ヒストグラムを生成、表示 

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai7_4.jpg) 
