# 第13回 レビュー
> **Note**[[link](_exp_1.ipynb)]  
## MP4V と H.264 の違い

MP4V は MPEG-4 Visual という動画フォーマットの一種で、H.264 は MPEG-4 AVC という動画フォーマットの一種です。

H.264の方が圧縮率が高く、高画質であるため、YouTubeや8Kテレビなどで使われています。



[8Kファイルフォーマットの動向と標準化への取り組み - NHK](https://www.nhk.or.jp/strl/publica/rd/177/3.html)





<figure><img src="../../images/34c37af45b3ea2f13838d416768d3c2d17dd91a8f260ddd6de7d266c057daa95.jpg"><figcaption>MP4Vで保存したとき</figcaption></figure>

<figure><img src="../../images/d3a938255c26a4195305e4000c72b9bb7c41211e3cb373bff3d7a0faa7bb7223.jpg"><figcaption>H264で保存したとき</figcaption></figure>

> **Note** [[link](_exp_1.ipynb)]  
### 設問5の解答例  

setメソッドの第二引数をframe_count+(定数)ではFPSによって巻き戻り・スキップする時間が変わってしまうため、frame_count+(fps*秒数)とすることで、動画のFPSに関わらず、5秒ずつスキップ・巻き戻しができます。  



```python

interval = 5

fps = cap.get(cv2.CAP_PROP_FPS)



while True:

    ret, frame = cap.read()

    frame_count = cap.get(cv2.CAP_PROP_POS_FRAMES)

    

    print(f"\r{frame_count}", end="")

    if ret == False:

        break

    

    cv2.putText(frame, str(frame_count), (10, 50), cv2.FONT_HERSHEY_TRIPLEX, 2, (0, 0, 0), 5)

    cv2.imshow("Video", frame)



    # 5秒戻る

    if cv2.waitKey(1) == ord("a"):

        cap.set(cv2.CAP_PROP_POS_FRAMES, frame_count-(fps*interval))



    # 5秒進む

    elif cv2.waitKey(1) == ord("d"):

        cap.set(cv2.CAP_PROP_POS_FRAMES, frame_count+(fps*interval))



    elif cv2.waitKey(1) == ord('q'):

        break



cv2.destroyAllWindows()

```

* FPSによっては、5秒巻き戻し、5秒スキップできない場合があります。[[link](image_processing7.ipynb)]  
* FPSによっては、5秒巻き戻し、5秒スキップできない場合があります。[[link](2023_05_29.ipynb)]  
