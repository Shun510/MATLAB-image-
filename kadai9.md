# 課題9レポート

標準画像「radio.jpg」を原画像とする．この画像は縦266画像，横400画素による長方形のディジタルカラー画像である．

ORG=imread('radio.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

以上のコマンドにより、原画像を白黒濃淡画像へ変換した結果を図１に示す．    

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai9_1.jpg)  
図1 原画像

以下のコマンドを用いて原画像にノイズを添付させる。図２に示す。

ORG = imnoise(ORG,'salt & pepper',0.02); % ノイズ添付  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai9_2.jpg)  
図2　 ノイズ付き原画像


平滑化フィルタを通し雑音除去を行う。使用したコマンドを以下に示し、その表示結果を図３に示す。

IMG = filter2(fspecial('average',3),ORG); % 平滑化フィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  
  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai9_3.jpg)  
図３　平滑化フィルタにより雑音除去をした原画像


また、メディアンフィルタでの雑音除去のコマンド、および結果を以下に示す。

IMG = medfilt2(ORG,[3 3]); % メディアンフィルタで雑音除去  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai9_4.jpg)  
図４　メディアンフィルタにより雑音除去をした画像




f=[0,-1,0;-1,5,-1;0,-1,0]; % フィルタの設計  
IMG = filter2(f,IMG,'same'); % フィルタの適用  
imagesc(IMG); colormap(gray); colorbar; % 画像の表示  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai9_5.jpg)  
図５　フィルタを適用した画像
