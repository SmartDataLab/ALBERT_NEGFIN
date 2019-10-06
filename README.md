# BERTFinanceNeg

BERT-based Finance Negation Detection

* Baseline for [金融信息负面及主体判定, CCF Big Data & Computing Intelligence Contest, CCF BDCI](https://www.datafountain.cn/competitions/353) * 
* [Chen Zhang](https://genezc.github.io).

* 2019-10-6: Jinhua Su plans to use ALBERT(Chinese) to improve its performance.
## Requirements

* Python 3.6
* PyTorch 1.0.0
* pytorch-pretrained-bert

## Usage

* Train with command, optional arguments could be found in [train.py](/train.py)
```bash
python train.py --model_name bert --batch_size 16 --save True 
```
* Infer with [infer.py](/infer.py)

## Model

An overview of the BERT-based baseline is given below

[ALBERT_ZH(Pytorch)](https://github.com/lonePatient/albert_pytorch)

[ALBERT_ZH(CHECHPOINT)](https://github.com/brightmart/albert_zh)

## INPUT
```python
for entity in entities:
    切割原文->(上文 + ' ' + entity + ' ' + 下文)
    input = ('[CLS]'+(上文 + ' ' + entity + ' ' + 下文)+'[SEP]'+entity+'[SEP]')
    output = bert(input)
    output_list.append(output)
```
## Linux_test

