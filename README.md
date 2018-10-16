# LOUPE_Keras

(Ongoing project)

Rewrite the LOUPE library (https://github.com/antoine77340/LOUPE) into Keras version. Many learnable pooling methods are covered. (NetVLAD, NetRVLAD, SoftDBoW, NetFV, CG)



## How to use? (Keras functional API)
```
import loupe_keras as lpk

# input x size: (batchsize,max_samples,feature_size)
# output x size: (batchsize, output_dim)
x = lpk.NetVLAD(feature_size=32, max_samples=20, cluster_size=3, output_dim=3*16)(x)
x = Reshape((3,16))(x)

```


## Ref
+ LOUPE library (https://github.com/antoine77340/LOUPE)

