# 課題8レポート

標準画像「radio.jpg」を原画像とする．この画像は縦266画像，横400画素による長方形のディジタルカラー画像である．

ORG=imread('radio.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

以上のコマンドにより、原画像を白黒濃淡画像へ変換した結果を図１に示す．    

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai8_1.jpg)  
図1 原画像

以下のコマンドを用いて原画像を閾値128で二値化した結果を、図２に示す  

IMG = ORG > 128; % 閾値128で二値化  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai8_2.jpg)  
図2　 閾値128で二値化した原画像


以下のコマンドを用いて、IMG内の連結要素のラベルを含むラベル行列IMGを返した結果を図３に示す。

IMG = bwlabeln(IMG);  
imagesc(IMG); colormap(jet); colorbar; % 画像の表示  


![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai8_3.jpg)  
図３　連結成分にラベルをつけした二値化された画像
