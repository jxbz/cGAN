<h1 align="center">
cGAN
</h1>

## CIFAR-10 class conditional GAN

The following Python packages are required: numpy, torch, torchvision, tqdm.

An example job is
```
python main.py --optim fromage --lrG 0.01 --lrD 0.01 --epochs 121 --seed 0
```
See inside `main.py` for additional command line arguments.

## Results

Runnning `sh batch.sh`, we obtain the following results:

|         | train FID  | test FID   |
|---------|------------|------------|
| Fromage | 16.4 ± 0.5 | 16.3 ± 0.8 |
| Adam    | 19.1 ± 0.9 | 19.4 ± 1.1 |
| SGD     | 36.4 ± 2.5 | 36.7 ± 2.7 |

## Acknowledgements
- The self attention block implementation is originally by https://github.com/zhaoyuzhi.
- The FID score implementation is by https://github.com/mseitzer/pytorch-fid.
- Thanks also go to [Jiahui Yu](https://jiahuiyu.com/).
- This codebase is from the [Fromage repository](https://github.com/jxbz/fromage), developed by Jeremy Bernstein, Arash Vahdat, Yisong Yue & Ming-Yu Liu.
 
## License
This repository (exluding the `fid/` subdirectory) is made available under a [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.
