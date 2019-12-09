# Final Test Accuracy :
```
10000/10000 [==============================] - 2s 189us/step
Test loss: 0.4663166994571686
Test accuracy: 0.911
```


# Model Summary: Resnet18
```
Model: "model_1"
__________________________________________________________________________________________________
Layer (type)                    Output Shape         Param #     Connected to                     
==================================================================================================
input_1 (InputLayer)            (None, 32, 32, 3)    0                                            
__________________________________________________________________________________________________
conv2d_1 (Conv2D)               (None, 32, 32, 32)   896         input_1[0][0]                    
__________________________________________________________________________________________________
batch_normalization_1 (BatchNor (None, 32, 32, 32)   128         conv2d_1[0][0]                   
__________________________________________________________________________________________________
activation_1 (Activation)       (None, 32, 32, 32)   0           batch_normalization_1[0][0]      
__________________________________________________________________________________________________
conv2d_2 (Conv2D)               (None, 32, 32, 32)   9248        activation_1[0][0]               
__________________________________________________________________________________________________
batch_normalization_2 (BatchNor (None, 32, 32, 32)   128         conv2d_2[0][0]                   
__________________________________________________________________________________________________
activation_2 (Activation)       (None, 32, 32, 32)   0           batch_normalization_2[0][0]      
__________________________________________________________________________________________________
conv2d_3 (Conv2D)               (None, 32, 32, 32)   9248        activation_2[0][0]               
__________________________________________________________________________________________________
batch_normalization_3 (BatchNor (None, 32, 32, 32)   128         conv2d_3[0][0]                   
__________________________________________________________________________________________________
add_1 (Add)                     (None, 32, 32, 32)   0           activation_1[0][0]               
                                                                 batch_normalization_3[0][0]      
__________________________________________________________________________________________________
activation_3 (Activation)       (None, 32, 32, 32)   0           add_1[0][0]                      
__________________________________________________________________________________________________
conv2d_4 (Conv2D)               (None, 32, 32, 32)   9248        activation_3[0][0]               
__________________________________________________________________________________________________
batch_normalization_4 (BatchNor (None, 32, 32, 32)   128         conv2d_4[0][0]                   
__________________________________________________________________________________________________
activation_4 (Activation)       (None, 32, 32, 32)   0           batch_normalization_4[0][0]      
__________________________________________________________________________________________________
conv2d_5 (Conv2D)               (None, 32, 32, 32)   9248        activation_4[0][0]               
__________________________________________________________________________________________________
batch_normalization_5 (BatchNor (None, 32, 32, 32)   128         conv2d_5[0][0]                   
__________________________________________________________________________________________________
add_2 (Add)                     (None, 32, 32, 32)   0           activation_3[0][0]               
                                                                 batch_normalization_5[0][0]      
__________________________________________________________________________________________________
activation_5 (Activation)       (None, 32, 32, 32)   0           add_2[0][0]                      
__________________________________________________________________________________________________
conv2d_6 (Conv2D)               (None, 32, 32, 32)   9248        activation_5[0][0]               
__________________________________________________________________________________________________
batch_normalization_6 (BatchNor (None, 32, 32, 32)   128         conv2d_6[0][0]                   
__________________________________________________________________________________________________
activation_6 (Activation)       (None, 32, 32, 32)   0           batch_normalization_6[0][0]      
__________________________________________________________________________________________________
conv2d_7 (Conv2D)               (None, 32, 32, 32)   9248        activation_6[0][0]               
__________________________________________________________________________________________________
batch_normalization_7 (BatchNor (None, 32, 32, 32)   128         conv2d_7[0][0]                   
__________________________________________________________________________________________________
add_3 (Add)                     (None, 32, 32, 32)   0           activation_5[0][0]               
                                                                 batch_normalization_7[0][0]      
__________________________________________________________________________________________________
activation_7 (Activation)       (None, 32, 32, 32)   0           add_3[0][0]                      
__________________________________________________________________________________________________
conv2d_8 (Conv2D)               (None, 16, 16, 64)   18496       activation_7[0][0]               
__________________________________________________________________________________________________
batch_normalization_8 (BatchNor (None, 16, 16, 64)   256         conv2d_8[0][0]                   
__________________________________________________________________________________________________
activation_8 (Activation)       (None, 16, 16, 64)   0           batch_normalization_8[0][0]      
__________________________________________________________________________________________________
conv2d_9 (Conv2D)               (None, 16, 16, 64)   36928       activation_8[0][0]               
__________________________________________________________________________________________________
conv2d_10 (Conv2D)              (None, 16, 16, 64)   2112        activation_7[0][0]               
__________________________________________________________________________________________________
batch_normalization_9 (BatchNor (None, 16, 16, 64)   256         conv2d_9[0][0]                   
__________________________________________________________________________________________________
add_4 (Add)                     (None, 16, 16, 64)   0           conv2d_10[0][0]                  
                                                                 batch_normalization_9[0][0]      
__________________________________________________________________________________________________
activation_9 (Activation)       (None, 16, 16, 64)   0           add_4[0][0]                      
__________________________________________________________________________________________________
conv2d_11 (Conv2D)              (None, 16, 16, 64)   36928       activation_9[0][0]               
__________________________________________________________________________________________________
batch_normalization_10 (BatchNo (None, 16, 16, 64)   256         conv2d_11[0][0]                  
__________________________________________________________________________________________________
activation_10 (Activation)      (None, 16, 16, 64)   0           batch_normalization_10[0][0]     
__________________________________________________________________________________________________
conv2d_12 (Conv2D)              (None, 16, 16, 64)   36928       activation_10[0][0]              
__________________________________________________________________________________________________
batch_normalization_11 (BatchNo (None, 16, 16, 64)   256         conv2d_12[0][0]                  
__________________________________________________________________________________________________
add_5 (Add)                     (None, 16, 16, 64)   0           activation_9[0][0]               
                                                                 batch_normalization_11[0][0]     
__________________________________________________________________________________________________
activation_11 (Activation)      (None, 16, 16, 64)   0           add_5[0][0]                      
__________________________________________________________________________________________________
conv2d_13 (Conv2D)              (None, 16, 16, 64)   36928       activation_11[0][0]              
__________________________________________________________________________________________________
batch_normalization_12 (BatchNo (None, 16, 16, 64)   256         conv2d_13[0][0]                  
__________________________________________________________________________________________________
activation_12 (Activation)      (None, 16, 16, 64)   0           batch_normalization_12[0][0]     
__________________________________________________________________________________________________
conv2d_14 (Conv2D)              (None, 16, 16, 64)   36928       activation_12[0][0]              
__________________________________________________________________________________________________
batch_normalization_13 (BatchNo (None, 16, 16, 64)   256         conv2d_14[0][0]                  
__________________________________________________________________________________________________
add_6 (Add)                     (None, 16, 16, 64)   0           activation_11[0][0]              
                                                                 batch_normalization_13[0][0]     
__________________________________________________________________________________________________
activation_13 (Activation)      (None, 16, 16, 64)   0           add_6[0][0]                      
__________________________________________________________________________________________________
conv2d_15 (Conv2D)              (None, 8, 8, 128)    73856       activation_13[0][0]              
__________________________________________________________________________________________________
batch_normalization_14 (BatchNo (None, 8, 8, 128)    512         conv2d_15[0][0]                  
__________________________________________________________________________________________________
activation_14 (Activation)      (None, 8, 8, 128)    0           batch_normalization_14[0][0]     
__________________________________________________________________________________________________
conv2d_16 (Conv2D)              (None, 8, 8, 128)    147584      activation_14[0][0]              
__________________________________________________________________________________________________
conv2d_17 (Conv2D)              (None, 8, 8, 128)    8320        activation_13[0][0]              
__________________________________________________________________________________________________
batch_normalization_15 (BatchNo (None, 8, 8, 128)    512         conv2d_16[0][0]                  
__________________________________________________________________________________________________
add_7 (Add)                     (None, 8, 8, 128)    0           conv2d_17[0][0]                  
                                                                 batch_normalization_15[0][0]     
__________________________________________________________________________________________________
activation_15 (Activation)      (None, 8, 8, 128)    0           add_7[0][0]                      
__________________________________________________________________________________________________
conv2d_18 (Conv2D)              (None, 8, 8, 128)    147584      activation_15[0][0]              
__________________________________________________________________________________________________
batch_normalization_16 (BatchNo (None, 8, 8, 128)    512         conv2d_18[0][0]                  
__________________________________________________________________________________________________
activation_16 (Activation)      (None, 8, 8, 128)    0           batch_normalization_16[0][0]     
__________________________________________________________________________________________________
conv2d_19 (Conv2D)              (None, 8, 8, 128)    147584      activation_16[0][0]              
__________________________________________________________________________________________________
batch_normalization_17 (BatchNo (None, 8, 8, 128)    512         conv2d_19[0][0]                  
__________________________________________________________________________________________________
add_8 (Add)                     (None, 8, 8, 128)    0           activation_15[0][0]              
                                                                 batch_normalization_17[0][0]     
__________________________________________________________________________________________________
activation_17 (Activation)      (None, 8, 8, 128)    0           add_8[0][0]                      
__________________________________________________________________________________________________
average_pooling2d_1 (AveragePoo (None, 1, 1, 128)    0           activation_17[0][0]              
__________________________________________________________________________________________________
flatten_1 (Flatten)             (None, 128)          0           average_pooling2d_1[0][0]        
__________________________________________________________________________________________________
dense_1 (Dense)                 (None, 10)           1290        flatten_1[0][0]                  
==================================================================================================
Total params: 792,330
Trainable params: 790,090
Non-trainable params: 2,240
```

# Logs
```
Epoch 1/50
Learning rate:  0.001
1563/1563 [==============================] - 57s 37ms/step - loss: 1.7082 - acc: 0.4726 - val_loss: 2.1516 - val_acc: 0.4369

Epoch 00001: val_acc improved from -inf to 0.43690, saving model to /content/saved_models/cifar10_ResNet20v1_model.001.h5
Epoch 2/50
Learning rate:  0.001
1563/1563 [==============================] - 52s 33ms/step - loss: 1.2716 - acc: 0.6363 - val_loss: 1.4888 - val_acc: 0.6008

Epoch 00002: val_acc improved from 0.43690 to 0.60080, saving model to /content/saved_models/cifar10_ResNet20v1_model.002.h5
Epoch 3/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 1.1154 - acc: 0.6932 - val_loss: 1.2923 - val_acc: 0.6645

Epoch 00003: val_acc improved from 0.60080 to 0.66450, saving model to /content/saved_models/cifar10_ResNet20v1_model.003.h5
Epoch 4/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 1.0231 - acc: 0.7294 - val_loss: 1.2483 - val_acc: 0.6766

Epoch 00004: val_acc improved from 0.66450 to 0.67660, saving model to /content/saved_models/cifar10_ResNet20v1_model.004.h5
Epoch 5/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.9689 - acc: 0.7505 - val_loss: 1.0199 - val_acc: 0.7470

Epoch 00005: val_acc improved from 0.67660 to 0.74700, saving model to /content/saved_models/cifar10_ResNet20v1_model.005.h5
Epoch 6/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.9212 - acc: 0.7679 - val_loss: 1.0041 - val_acc: 0.7515

Epoch 00006: val_acc improved from 0.74700 to 0.75150, saving model to /content/saved_models/cifar10_ResNet20v1_model.006.h5
Epoch 7/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.8906 - acc: 0.7794 - val_loss: 0.9047 - val_acc: 0.7912

Epoch 00007: val_acc improved from 0.75150 to 0.79120, saving model to /content/saved_models/cifar10_ResNet20v1_model.007.h5
Epoch 8/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.8632 - acc: 0.7914 - val_loss: 0.8481 - val_acc: 0.8065

Epoch 00008: val_acc improved from 0.79120 to 0.80650, saving model to /content/saved_models/cifar10_ResNet20v1_model.008.h5
Epoch 9/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.8435 - acc: 0.7985 - val_loss: 1.0865 - val_acc: 0.7410

Epoch 00009: val_acc did not improve from 0.80650
Epoch 10/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.8245 - acc: 0.8055 - val_loss: 0.9114 - val_acc: 0.7875

Epoch 00010: val_acc did not improve from 0.80650
Epoch 11/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.8073 - acc: 0.8110 - val_loss: 0.8425 - val_acc: 0.8078

Epoch 00011: val_acc improved from 0.80650 to 0.80780, saving model to /content/saved_models/cifar10_ResNet20v1_model.011.h5
Epoch 12/50
Learning rate:  0.001
1563/1563 [==============================] - 50s 32ms/step - loss: 0.7973 - acc: 0.8129 - val_loss: 0.8498 - val_acc: 0.8131

Epoch 00012: val_acc improved from 0.80780 to 0.81310, saving model to /content/saved_models/cifar10_ResNet20v1_model.012.h5
Epoch 13/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7814 - acc: 0.8206 - val_loss: 1.0141 - val_acc: 0.7705

Epoch 00013: val_acc did not improve from 0.81310
Epoch 14/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7695 - acc: 0.8253 - val_loss: 0.7727 - val_acc: 0.8297

Epoch 00014: val_acc improved from 0.81310 to 0.82970, saving model to /content/saved_models/cifar10_ResNet20v1_model.014.h5
Epoch 15/50
Learning rate:  0.001
1563/1563 [==============================] - 50s 32ms/step - loss: 0.7658 - acc: 0.8252 - val_loss: 0.8642 - val_acc: 0.8065

Epoch 00015: val_acc did not improve from 0.82970
Epoch 16/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7559 - acc: 0.8294 - val_loss: 0.7888 - val_acc: 0.8212

Epoch 00016: val_acc did not improve from 0.82970
Epoch 17/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.7463 - acc: 0.8309 - val_loss: 0.7945 - val_acc: 0.8218

Epoch 00017: val_acc did not improve from 0.82970
Epoch 18/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7370 - acc: 0.8360 - val_loss: 0.7819 - val_acc: 0.8307

Epoch 00018: val_acc improved from 0.82970 to 0.83070, saving model to /content/saved_models/cifar10_ResNet20v1_model.018.h5
Epoch 19/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7308 - acc: 0.8395 - val_loss: 0.7688 - val_acc: 0.8354

Epoch 00019: val_acc improved from 0.83070 to 0.83540, saving model to /content/saved_models/cifar10_ResNet20v1_model.019.h5
Epoch 20/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7235 - acc: 0.8414 - val_loss: 0.8144 - val_acc: 0.8174

Epoch 00020: val_acc did not improve from 0.83540
Epoch 21/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7165 - acc: 0.8437 - val_loss: 0.9115 - val_acc: 0.8031

Epoch 00021: val_acc did not improve from 0.83540
Epoch 22/50
Learning rate:  0.001
1563/1563 [==============================] - 50s 32ms/step - loss: 0.7156 - acc: 0.8407 - val_loss: 0.7955 - val_acc: 0.8233

Epoch 00022: val_acc did not improve from 0.83540
Epoch 23/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.7070 - acc: 0.8466 - val_loss: 0.8759 - val_acc: 0.8043

Epoch 00023: val_acc did not improve from 0.83540
Epoch 24/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.7033 - acc: 0.8455 - val_loss: 0.7830 - val_acc: 0.8295

Epoch 00024: val_acc did not improve from 0.83540
Epoch 25/50
Learning rate:  0.001
1563/1563 [==============================] - 50s 32ms/step - loss: 0.6987 - acc: 0.8475 - val_loss: 0.7063 - val_acc: 0.8455

Epoch 00025: val_acc improved from 0.83540 to 0.84550, saving model to /content/saved_models/cifar10_ResNet20v1_model.025.h5
Epoch 26/50
Learning rate:  0.001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.6903 - acc: 0.8494 - val_loss: 0.9004 - val_acc: 0.7988

Epoch 00026: val_acc did not improve from 0.84550
Epoch 27/50
Learning rate:  0.0001
1563/1563 [==============================] - 50s 32ms/step - loss: 0.5857 - acc: 0.8859 - val_loss: 0.5455 - val_acc: 0.8993

Epoch 00027: val_acc improved from 0.84550 to 0.89930, saving model to /content/saved_models/cifar10_ResNet20v1_model.027.h5
Epoch 28/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.5419 - acc: 0.8965 - val_loss: 0.5390 - val_acc: 0.8995

Epoch 00028: val_acc improved from 0.89930 to 0.89950, saving model to /content/saved_models/cifar10_ResNet20v1_model.028.h5
Epoch 29/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.5153 - acc: 0.9044 - val_loss: 0.5192 - val_acc: 0.9035

Epoch 00029: val_acc improved from 0.89950 to 0.90350, saving model to /content/saved_models/cifar10_ResNet20v1_model.029.h5
Epoch 30/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.5030 - acc: 0.9074 - val_loss: 0.5156 - val_acc: 0.9066

Epoch 00030: val_acc improved from 0.90350 to 0.90660, saving model to /content/saved_models/cifar10_ResNet20v1_model.030.h5
Epoch 31/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4858 - acc: 0.9109 - val_loss: 0.5012 - val_acc: 0.9079

Epoch 00031: val_acc improved from 0.90660 to 0.90790, saving model to /content/saved_models/cifar10_ResNet20v1_model.031.h5
Epoch 32/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4713 - acc: 0.9131 - val_loss: 0.4884 - val_acc: 0.9099

Epoch 00032: val_acc improved from 0.90790 to 0.90990, saving model to /content/saved_models/cifar10_ResNet20v1_model.032.h5
Epoch 33/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4619 - acc: 0.9164 - val_loss: 0.4944 - val_acc: 0.9086

Epoch 00033: val_acc did not improve from 0.90990
Epoch 34/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4494 - acc: 0.9183 - val_loss: 0.4800 - val_acc: 0.9109

Epoch 00034: val_acc improved from 0.90990 to 0.91090, saving model to /content/saved_models/cifar10_ResNet20v1_model.034.h5
Epoch 35/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 33ms/step - loss: 0.4424 - acc: 0.9189 - val_loss: 0.4811 - val_acc: 0.9083

Epoch 00035: val_acc did not improve from 0.91090
Epoch 36/50
Learning rate:  0.0001
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4339 - acc: 0.9201 - val_loss: 0.4763 - val_acc: 0.9090

Epoch 00036: val_acc did not improve from 0.91090
Epoch 37/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4216 - acc: 0.9250 - val_loss: 0.4728 - val_acc: 0.9084

Epoch 00037: val_acc did not improve from 0.91090
Epoch 38/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4219 - acc: 0.9249 - val_loss: 0.4713 - val_acc: 0.9090

Epoch 00038: val_acc did not improve from 0.91090
Epoch 39/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4194 - acc: 0.9248 - val_loss: 0.4703 - val_acc: 0.9092

Epoch 00039: val_acc did not improve from 0.91090
Epoch 40/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 33ms/step - loss: 0.4198 - acc: 0.9250 - val_loss: 0.4691 - val_acc: 0.9097

Epoch 00040: val_acc did not improve from 0.91090
Epoch 41/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4205 - acc: 0.9250 - val_loss: 0.4688 - val_acc: 0.9100

Epoch 00041: val_acc did not improve from 0.91090
Epoch 42/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4159 - acc: 0.9270 - val_loss: 0.4675 - val_acc: 0.9099

Epoch 00042: val_acc did not improve from 0.91090
Epoch 43/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4156 - acc: 0.9262 - val_loss: 0.4675 - val_acc: 0.9110

Epoch 00043: val_acc improved from 0.91090 to 0.91100, saving model to /content/saved_models/cifar10_ResNet20v1_model.043.h5
Epoch 44/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4142 - acc: 0.9266 - val_loss: 0.4685 - val_acc: 0.9100

Epoch 00044: val_acc did not improve from 0.91100
Epoch 45/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4167 - acc: 0.9261 - val_loss: 0.4661 - val_acc: 0.9105

Epoch 00045: val_acc did not improve from 0.91100
Epoch 46/50
Learning rate:  1e-06
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4097 - acc: 0.9280 - val_loss: 0.4649 - val_acc: 0.9106

Epoch 00046: val_acc did not improve from 0.91100
Epoch 47/50
Learning rate:  5e-07
1563/1563 [==============================] - 51s 33ms/step - loss: 0.4127 - acc: 0.9280 - val_loss: 0.4654 - val_acc: 0.9110

Epoch 00047: val_acc did not improve from 0.91100
Epoch 48/50
Learning rate:  5e-07
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4122 - acc: 0.9286 - val_loss: 0.4659 - val_acc: 0.9109

Epoch 00048: val_acc did not improve from 0.91100
Epoch 49/50
Learning rate:  5e-07
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4145 - acc: 0.9266 - val_loss: 0.4650 - val_acc: 0.9118

Epoch 00049: val_acc improved from 0.91100 to 0.91180, saving model to /content/saved_models/cifar10_ResNet20v1_model.049.h5
Epoch 50/50
Learning rate:  5e-07
1563/1563 [==============================] - 51s 32ms/step - loss: 0.4133 - acc: 0.9272 - val_loss: 0.4663 - val_acc: 0.9110

Epoch 00050: val_acc did not improve from 0.91180

```


