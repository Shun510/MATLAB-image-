# 課題3レポート

標準画像「radio.jpg」を原画像とする．この画像は縦266画像，横400画素による長方形のディジタルカラー画像である．

ORG=imread('radio.jpg'); % 原画像の入力
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換
imagesc(ORG); colormap(gray); colorbar; % 画像の表示

以上のコマンドにより、表示した結果を図１に示す．

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai4_1.jpg)  
 　　　　　　　　　　　　　　　　　　　図1 原画像

次に、以下のコマンドを用いて図１のヒストグラムを表示させた結果を、図２に示す
imhist(ORG); % ヒストグラムの表示

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai4_2.jpg)  
図2 ヒストグラム
