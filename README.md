# opencv-face-analysis

手动打标识别区域，生成多种检测分析结果的代码

- [opencv-face-analysis](#opencv-face-analysis)
  - [部署运行](#部署运行)
    - [pixi](#pixi)
    - [conda](#conda)
  - [使用](#使用)


## 部署运行

下载，解压 [shape_predictor_68_face_landmarks.dat](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)

### pixi

```bash
pixi run jupyter notebook
```

### conda

```bash
conda create --file=./environment_win.yaml
conda run -n opencv jupyter notebook
```

## 使用

除以下五个脚本，其他只需准备 `imgs/{1,2,3,4,5}.jpg` 五张图片

使用 [labelme](https://github.com/wkentaro/labelme) 对图片进行多边形打标，0为人脸，1为全身

存储对应的json文件到 `imgs/` 中。（1.json，2.json，...）

先运行 `图像检测处理.ipynb` ，即可运行 `面部特征数据.ipynb`/`形态学操作.ipynb`/`人脸图片进行图像处理.ipynb`

打标之后也可运行 `绘制区域颜色.ipynb`
