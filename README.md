# LOUPE_Keras

(Ongoing project. If you find any bug, please inform me in the issue. Thanks)

Rewrite the LOUPE library (https://github.com/antoine77340/LOUPE) into Keras version. Many learnable pooling or differentiable aggregation methods are covered. (NetVLAD, NetRVLAD, SoftDBoW, NetFV, CG)



## How to use? (Keras functional API)
```
import loupe_keras as lpk

# input x size: (batchsize, max_samples, feature_size)
# output x size: (batchsize, output_dim)
x = lpk.NetVLAD(feature_size=32, max_samples=20, cluster_size=3, output_dim=3*16)(x)
x = Reshape((3,16))(x)

```


## Ref
+ LOUPE library (https://github.com/antoine77340/LOUPE)
+ Arandjelovic, Relja and Gronat, Petre and Torii, Akihiko and Pajdla, Tomas and Sivic, Josef, NetVLAD: CNN architecture for weakly supervised place recognition, CVPR 2016
+ Antoine Miech and Ivan Laptev and Josef Sivic, Learnable pooling with Context Gating for video classification, arXiv:1706.06905
