参考： [NVIDIA/tacotron2](https://github.com/NVIDIA/tacotron2)

## 如何使用
1. 将原始日语文本放入 ./filelists
2. 将WAV文件放入 ./wav
3. (可选) 下载NVIDIA的[pretrained模型](https://drive.google.com/file/d/1c5ZTuT7J08wLUoVZ2KkUs_VdZuJ86ZqA/view?usp=sharing)
4. 打开./train.ipynb来安装依赖并开始训练。
5. 下载NVIDIA的[WaveGlow模型](https://drive.google.com/open?id=1rpK8CzAAirq9sWZhe9nlfvxMF1dRgFbF)
6. 打开./inference.ipynb来生成语音

## 类别

文件 ./hparams.py 第30行
### 1. 'japanese_cleaners'

#### 之前

何かあったらいつでも話して下さい。学院のことじゃなく、私事に関することでも何でも
#### 之后
nanikaacltaraitsudemohanashItekudasai.gakuiNnokotojanaku,shijinikaNsurukotodemonanidemo.
### 2. 'japanese_tokenization_cleaners'
#### 之前
何かあったらいつでも話して下さい。学院のことじゃなく、私事に関することでも何でも
#### 之后
nani ka acl tara itsu demo hanashi te kudasai. gakuiN no koto ja naku, shiji nikaNsuru koto de mo naNdemo.
### 3. 'japanese_accent_cleaners'
#### 之前
何かあったらいつでも話して下さい。学院のことじゃなく、私事に関することでも何でも
#### 之后
:na)nika a)cltara i)tsudemo ha(na)shIte ku(dasa)i.:ga(kuiNno ko(to)janaku,:shi)jini ka(Nsu)ru ko(to)demo na)nidemo.
### 4. 'japanese_phrase_cleaners'
#### 之前
何かあったらいつでも話して下さい。学院のことじゃなく、私事に関することでも何でも
#### 之后
nanika acltara itsudemo hanashIte kudasai. gakuiNno kotojanaku, shijini kaNsuru kotodemo nanidemo.

## 模型

记得在进行./inference.ipynb 更改这行
```python
sequence = np.array(text_to_sequence(text, ['japanese_cleaners']))[None, :]
```
### 查看更多
### 魔女的夜宴

#### 绫地宁宁

* [Model 1](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/ESltqOvyK3ZPsLMQwpv5FH0BoX8slLVsz3eUKwHHKkg9ww?e=vc5fdd) ['japanese_cleaners']
* [Model 2](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/ETNLDYH_ZRpMmNR0VGALhNQB5-LiJOqTaWQz8tXtbvCV-g?e=7nf2Ec) ['japanese_tokenization_cleaners']
* [Model 3](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/Eb0WROtOsYBInTmQQZHf36IBSXmyVd4JiCF7OnQjOZkjGg?e=qbbsv4) ['japanese_accent_cleaners']

#### 因幡巡

* [Model 1](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/Ed29Owd-E1NKstl_EFGZFVABe-F-a65jSAefeW_uEQuWxw?e=J628nT) ['japanese_tokenization_cleaners']
* [Model 2](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/ER8C2tiu4-RPi_MtQ3TCuTkBVRvO1MgJOPAKpAUD4ZLiow?e=ktT81t) ['japanese_tokenization_cleaners']

### 千恋＊万花

#### 朝武芳乃

* [Model 1](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/EdfFetSH3tpMr7nkiqAKzwEBXjuCRICcvgUortEvE4pdjw?e=UyvkyI) ['japanese_tokenization_cleaners']
* [Model 2](https://sjtueducn-my.sharepoint.com/:u:/g/personal/cjang_cjengh_sjtu_edu_cn/EeE4h5teC5xKms1VRnaNiW8BuqslFeR8VW7bCk7SWh2r8w?e=qADqbu) ['japanese_phrase_cleaners']
