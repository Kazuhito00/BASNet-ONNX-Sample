# BASNet-ONNX-Sample
<img src="https://user-images.githubusercontent.com/37477845/143734485-b6d1d032-b05e-487f-82fa-0c959dba8402.gif" width="75%"><br>
<img src="https://user-images.githubusercontent.com/37477845/143734801-d01dd064-dd51-4e89-bbd1-bd9ec9dc55bc.png" width="75%"><br>
[BASNet](https://github.com/xuebinqin/BASNet)(Salient Object Detection)のPythonでのONNX推論サンプルです。<br>
ONNXに変換したモデルも同梱しています。<br>
変換自体を試したい方はColaboratoryなどで[BASNet_Convert2ONNX.ipynb](BASNet_Convert2ONNX.ipynb)を使用ください。<br>

# Requirement(ONNX変換)
* Pytorch 1.9.0 or later
* onnx 1.10.2 or later
* onnx-simplifier 0.3.6 or later

# Requirement(ONNX推論)
* gdown 4.2.0 or later
* OpenCV 4.5.3.56 or later
* onnxruntime-gpu 1.9.0 or later <br>※onnxruntimeでも動作しますが、推論時間がかかるのでGPUをお勧めします

# Demo
デモの実行方法は以下です。<br>
デモ実行前に、[Googleドライブ](https://drive.google.com/uc?id=1GG40AzPpT74GdO0jQi9L5lnS8g68TRbP)からbasnet.onnxをダウンロードし、modelディレクトリに格納してください。<br>
basnet.onnxが格納されていない場合、gdownを用いたダウンロードが実行されます(gdownインストール必要)
```bash
python sample_onnx.py
```
* --device<br>
カメラデバイス番号の指定<br>
デフォルト：0
* --movie<br>
動画ファイルの指定 ※指定時はカメラデバイスより優先<br>
デフォルト：指定なし
* --width<br>
カメラキャプチャ時の横幅<br>
デフォルト：640
* --height<br>
カメラキャプチャ時の縦幅<br>
デフォルト：360
* --model<br>
ロードするモデルの格納パス<br>
デフォルト：model/basnet.onnx
* --input_shape<br>
モデルの入力サイズ<br>
デフォルト：256

# Reference
* [xuebinqin/BASNet](https://github.com/xuebinqin/BASNet)

# Author
高橋かずひと(https://twitter.com/KzhtTkhs)
 
# License 
BASNet-ONNX-Sample is under [MIT License](LICENSE).

# License(Image)
猫の画像は[フリー素材ぱくたそ](https://www.pakutaso.com)様の写真を利用しています。
