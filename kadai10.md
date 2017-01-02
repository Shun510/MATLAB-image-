# 課題10レポート

標準画像「radio.jpg」を原画像とする．この画像は縦266画像，横400画素による長方形のディジタルカラー画像である．

ORG=imread('radio.jpg'); % 原画像の入力  
ORG= rgb2gray(ORG); % カラー画像を白黒濃淡画像へ変換  
imagesc(ORG); colormap(gray); colorbar; % 画像の表示  

以上のコマンドにより、原画像を白黒濃淡画像へ変換した結果を図１に示す．    

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai10_1.jpg)  
図1 原画像

次のそれぞれのプログラムを用いて、エッジ抽出を体験する。


・プレウィット法によるエッジ抽出。

  IMG = edge(ORG,'prewitt'); % エッジ抽出（プレウィット法）  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai10_2.jpg)  
図2　 プレウィット法


・ソベル法によるエッジ抽出

  IMG = edge(ORG,'sobel'); % エッジ抽出（ソベル法）  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai10_3.jpg)  
図３　ソベル法


・キャニー法によるエッジ抽出

  IMG = edge(ORG,'canny'); % エッジ抽出（キャニー法）  

![原画像](https://github.com/Shun510/MATLAB2/blob/master/images/kadai10_4.jpg)  
図４　キャニー法

