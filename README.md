## 项目介绍
本项目可以直接将`qmcflac`文件转换成`mp3`文件，目前支持并发执行

## 执行方式
```bash
python qmcflac.py -o /tmp/mp3_dir -i /tmp/qmcflac_dir
```
在这里
```bash
-o: 转换mp3输出目录
-i: 原始qmcflac目录
-n: 转换文件的进程数，如果不指定，脚本会自动根据转换数量自动决定进程数
-m: 可以输入"qmc2mp3": 代表qmcflac格式转换成flac/"flac2mp3": 代表flac格式转换成mp3/"qmc2flac": 代表qmcflac格式转换成mp3，三种模式，不指定，则默认为"qmc2mp3"
```

## 感谢
在这里直接使用了两个开源项目。找过其他实现方案，只有`flac2mp3`这个方案不依赖`ffmpeg`环境，因此使用上不需要过多安装其他依赖库，另外通过
多进程的包装，执行效率也比原项目直接执行更快。
```bash
qmc->flac: https://github.com/Presburger/qmc-decoder
flac->mp3: https://github.com/robinbowes/flac2mp3
```
##  补充
macOS环境下需要添加的包
flac,lame包需要再安装
```bash
brew install flac
brew install flam
```
