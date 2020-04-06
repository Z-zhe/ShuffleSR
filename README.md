# ShuffleSR

- <strong>Lighter</strong> and <strong>better</strong> image super-resolution algorithm than [WDSR](https://github.com/JiahuiYu/wdsr_ntire2018)

<br>

## Performance

- Training and validation results on [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/) dataset

**DIV2K Mild X4**

|name|PSNR|SSIM|Flops|parms|
|:---|:---|:---|:---|:---|
|Bicubic|17.6147|0.4268|-|-|
|ShuffleSR|18.7887|0.4857|<strong>126.5M</strong>|<strong>56.5K</strong>|
|ShuffleSR_SE|<strong>18.8280</strong>|0.5078|128.2M|158.9K|
|ShuffleSR_SK|18.7890|<strong>0.5094</strong>|165.0M|152.2K|
|WDSR|18.7983|0.5072|381.5M|167.7K|
|ShuffleSR_M|18.8009|0.5082|342.4M|152.1K|

<br>

**DIV2K Unknown X4**

|name|PSNR|SSIM|Flops|parms|
|:---|:---|:---|:---|:---|
|Bicubic|21.7511|0.5561|-|-|
|ShuffleSR|24.8454|0.7059|<strong>129.2M</strong>|<strong>58.4K</strong>|
|ShuffleSR_SK|<strong>26.4377</strong>|<strong>0.7542</strong>|165.0M|152.2K|
|ShuffleSR_SE|25.6780|0.7292|128.2M|158.9K|
|WDSR|25.2512|0.7152|381.5M|167.7K|
|ShuffleSR_M|25.4469|0.7267|342.4M|152.1K|

<br>

## Usage
- Git clone

```
cd /path/to/ShuffleSR
```

<br>

- Install requirement

```
pip install -r requirement.txt
```

<br>

- Download data set [DIV2K](https://data.vision.ee.ethz.ch/cvl/DIV2K/)

**Replace '/path/to/xx' in the code with your path**

<br>

- Train
```
help:
python train.py -h

examples:
python train.py --network ShuffleSR_SE --features 32 --expand 3 --block 8
python train.py --network ShuffleSR --features 32 --expand 6 --block 8 --lr 0.001
python train.py --network WDSR --features 32 --expand 3 --block 8 --epochs 100
```

<br>

- Test

**set `model_path` and `output_path` in the `output.py`** 
 
```
python output.py
```

<br>

## ShuffleSR SR result

### DIV2K Unknown X4 
- 0825.png

![0825.png](./show/unknown_output/0825.png)

<br>

- 0826.png

![0826.png](./show/unknown_output/0826.png)

<br>

- 0827.png

![0827.png](./show/unknown_output/0827.png)

<br>

- 0832.png

![0832.png](./show/unknown_output/0832.png)

<br>

### DIV2K Mild X4 

- 0836.png

![0826.png](./show/mild_output/0836.png)

<br>

- 0844.png

![0827.png](./show/mild_output/0844.png)

<br>

- 0898.png

![0832.png](./show/mild_output/0898.png)