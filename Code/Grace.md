# Grace

## python使用相关

### sys.args的使用

命令行使用即可

```python
import sys
a = args[0]
b = args[1]
```

## Torch相关

### 设置相同的seed来保证输出的一致性

```python
	#设置CPU生成随机数的种子，方便下次复现实验结果。
    =torch.manual_seed(args.seed)
    #设置随机数种子，作用为使随机生成的数据可预测。
    np.random.seed(args.seed)
    #而当seed()有参数时，每次生成的随机数是一样的
    random.seed(args.seed + t)
    #为特定GPU设置种子，生成随机数 为所有GPU设置种子，生成随机数
    torch.cuda.manual_seed(args.seed)
    torch.cuda.manual_seed_all(args.seed)
    #保证每次运行网络的时候相同输入的输出是固定的
    torch.backends.cudnn.deterministic = True
```

