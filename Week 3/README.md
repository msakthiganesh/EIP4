### Final Validation Accuracy of Base Network: 81.75

## Model Definition:

```python
model = Sequential()

model.add(SeparableConv2D(32, (3, 3), padding='same', input_shape=(32, 32, 3))) # O/P Size: 32x32x32 , RF:3X3
model.add(Activation('relu'))

model.add(SeparableConv2D(32, (3, 3), padding='same')) # O/P Size: 32x32x32 , RF:5X5
model.add(Activation('relu'))
model.add(BatchNormalization())

model.add(MaxPooling2D(pool_size=(2, 2))) # O/P Size: 16x16x32 , RF:6X6
model.add(Dropout(0.1))

model.add(SeparableConv2D(64, (3, 3), padding='same')) # O/P Size: 16x16x64 , RF:10X10
model.add(Activation('relu'))
model.add(BatchNormalization())

model.add(SeparableConv2D(64, (3, 3), padding='same'))# O/P Size: 16x16x64, RF:14x14
model.add(BatchNormalization())
model.add(Activation('relu'))

model.add(MaxPooling2D(pool_size=(2, 2)))# O/P Size: 8x8x64, RF:16x16
model.add(Dropout(0.1))

model.add(SeparableConv2D(128, (3, 3), padding='same'))# O/P Size: 8x8x128, RF:24x24
model.add(Activation('relu'))

model.add(BatchNormalization())

model.add(SeparableConv2D(128, (3, 3), padding='same'))# O/P Size: 8x8x128, RF:32x32
model.add(Activation('relu'))
model.add(BatchNormalization())

model.add(MaxPooling2D(pool_size=(2, 2))) #O/P Size: 4x4x128, RF:36X36
model.add(Dropout(0.1))

model.add(SeparableConv2D(256, (3, 3), padding='same'))# O/P Size: 4x4x256, RF:52x52
model.add(Activation('relu'))
model.add(BatchNormalization())

model.add(SeparableConv2D(10, (3, 3),padding='same'))# O/P Size: 4x4x10 ,RF:68x68
model.add(Activation('relu'))
model.add(BatchNormalization())
model.add(Dropout(0.1))

model.add(SeparableConv2D(10, 4))
model.add(Flatten())
model.add(Activation('softmax'))
```

## Model Summary:
```
Model: "sequential_1"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
separable_conv2d_1 (Separabl (None, 32, 32, 32)        155       
_________________________________________________________________
activation_1 (Activation)    (None, 32, 32, 32)        0         
_________________________________________________________________
separable_conv2d_2 (Separabl (None, 32, 32, 32)        1344      
_________________________________________________________________
activation_2 (Activation)    (None, 32, 32, 32)        0         
_________________________________________________________________
batch_normalization_1 (Batch (None, 32, 32, 32)        128       
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 16, 16, 32)        0         
_________________________________________________________________
dropout_1 (Dropout)          (None, 16, 16, 32)        0         
_________________________________________________________________
separable_conv2d_3 (Separabl (None, 16, 16, 64)        2400      
_________________________________________________________________
activation_3 (Activation)    (None, 16, 16, 64)        0         
_________________________________________________________________
batch_normalization_2 (Batch (None, 16, 16, 64)        256       
_________________________________________________________________
separable_conv2d_4 (Separabl (None, 16, 16, 64)        4736      
_________________________________________________________________
batch_normalization_3 (Batch (None, 16, 16, 64)        256       
_________________________________________________________________
activation_4 (Activation)    (None, 16, 16, 64)        0         
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 8, 8, 64)          0         
_________________________________________________________________
dropout_2 (Dropout)          (None, 8, 8, 64)          0         
_________________________________________________________________
separable_conv2d_5 (Separabl (None, 8, 8, 128)         8896      
_________________________________________________________________
activation_5 (Activation)    (None, 8, 8, 128)         0         
_________________________________________________________________
batch_normalization_4 (Batch (None, 8, 8, 128)         512       
_________________________________________________________________
separable_conv2d_6 (Separabl (None, 8, 8, 128)         17664     
_________________________________________________________________
activation_6 (Activation)    (None, 8, 8, 128)         0         
_________________________________________________________________
batch_normalization_5 (Batch (None, 8, 8, 128)         512       
_________________________________________________________________
max_pooling2d_3 (MaxPooling2 (None, 4, 4, 128)         0         
_________________________________________________________________
dropout_3 (Dropout)          (None, 4, 4, 128)         0         
_________________________________________________________________
separable_conv2d_7 (Separabl (None, 4, 4, 256)         34176     
_________________________________________________________________
activation_7 (Activation)    (None, 4, 4, 256)         0         
_________________________________________________________________
batch_normalization_6 (Batch (None, 4, 4, 256)         1024      
_________________________________________________________________
separable_conv2d_8 (Separabl (None, 4, 4, 10)          4874      
_________________________________________________________________
activation_8 (Activation)    (None, 4, 4, 10)          0         
_________________________________________________________________
batch_normalization_7 (Batch (None, 4, 4, 10)          40        
_________________________________________________________________
dropout_4 (Dropout)          (None, 4, 4, 10)          0         
_________________________________________________________________
separable_conv2d_9 (Separabl (None, 1, 1, 10)          270       
_________________________________________________________________
flatten_1 (Flatten)          (None, 10)                0         
_________________________________________________________________
activation_9 (Activation)    (None, 10)                0         
=================================================================
Total params: 77,243
Trainable params: 75,879
Non-trainable params: 1,364
_________________________________________________________________
```
## Log:
```
Epoch 1/50

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
390/390 [==============================] - 13s 35ms/step - loss: 1.3913 - acc: 0.4994 - val_loss: 2.2215 - val_acc: 0.4184
Epoch 2/50

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
390/390 [==============================] - 8s 20ms/step - loss: 1.0097 - acc: 0.6404 - val_loss: 1.1083 - val_acc: 0.6115
Epoch 3/50

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
390/390 [==============================] - 8s 20ms/step - loss: 0.8643 - acc: 0.6933 - val_loss: 1.7361 - val_acc: 0.4513
Epoch 4/50

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
390/390 [==============================] - 8s 20ms/step - loss: 0.7789 - acc: 0.7234 - val_loss: 0.8291 - val_acc: 0.7069
Epoch 5/50

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
390/390 [==============================] - 8s 20ms/step - loss: 0.7205 - acc: 0.7465 - val_loss: 0.7528 - val_acc: 0.7395
Epoch 6/50

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
390/390 [==============================] - 8s 20ms/step - loss: 0.6706 - acc: 0.7653 - val_loss: 0.8025 - val_acc: 0.7266
Epoch 7/50

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
390/390 [==============================] - 8s 20ms/step - loss: 0.6464 - acc: 0.7726 - val_loss: 0.8181 - val_acc: 0.7176
Epoch 8/50

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
390/390 [==============================] - 8s 20ms/step - loss: 0.6120 - acc: 0.7853 - val_loss: 0.7602 - val_acc: 0.7392
Epoch 9/50

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
390/390 [==============================] - 8s 20ms/step - loss: 0.5873 - acc: 0.7940 - val_loss: 0.7823 - val_acc: 0.7387
Epoch 10/50

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
390/390 [==============================] - 8s 20ms/step - loss: 0.5678 - acc: 0.8003 - val_loss: 0.7675 - val_acc: 0.7442
Epoch 11/50

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
390/390 [==============================] - 8s 20ms/step - loss: 0.5433 - acc: 0.8091 - val_loss: 0.6183 - val_acc: 0.7900
Epoch 12/50

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
390/390 [==============================] - 8s 20ms/step - loss: 0.5332 - acc: 0.8121 - val_loss: 0.5975 - val_acc: 0.7957
Epoch 13/50

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
390/390 [==============================] - 8s 19ms/step - loss: 0.5208 - acc: 0.8164 - val_loss: 0.6233 - val_acc: 0.7887
Epoch 14/50

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
390/390 [==============================] - 8s 20ms/step - loss: 0.5033 - acc: 0.8223 - val_loss: 0.6507 - val_acc: 0.7865
Epoch 15/50

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
390/390 [==============================] - 8s 20ms/step - loss: 0.4892 - acc: 0.8279 - val_loss: 0.6472 - val_acc: 0.7823
Epoch 16/50

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
390/390 [==============================] - 8s 20ms/step - loss: 0.4810 - acc: 0.8297 - val_loss: 0.5564 - val_acc: 0.8103
Epoch 17/50

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
390/390 [==============================] - 8s 19ms/step - loss: 0.4685 - acc: 0.8346 - val_loss: 0.5863 - val_acc: 0.8016
Epoch 18/50

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
390/390 [==============================] - 8s 20ms/step - loss: 0.4659 - acc: 0.8348 - val_loss: 0.5567 - val_acc: 0.8131
Epoch 19/50

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
390/390 [==============================] - 8s 20ms/step - loss: 0.4514 - acc: 0.8397 - val_loss: 0.5771 - val_acc: 0.8049
Epoch 20/50

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
390/390 [==============================] - 8s 20ms/step - loss: 0.4511 - acc: 0.8407 - val_loss: 0.5864 - val_acc: 0.8086
Epoch 21/50

Epoch 00021: LearningRateScheduler setting learning rate to 0.0004065041.
390/390 [==============================] - 7s 19ms/step - loss: 0.4406 - acc: 0.8452 - val_loss: 0.5628 - val_acc: 0.8149
Epoch 22/50

Epoch 00022: LearningRateScheduler setting learning rate to 0.000389661.
390/390 [==============================] - 8s 20ms/step - loss: 0.4337 - acc: 0.8479 - val_loss: 0.5998 - val_acc: 0.7981
Epoch 23/50

Epoch 00023: LearningRateScheduler setting learning rate to 0.0003741581.
390/390 [==============================] - 7s 19ms/step - loss: 0.4285 - acc: 0.8491 - val_loss: 0.6112 - val_acc: 0.8007
Epoch 24/50

Epoch 00024: LearningRateScheduler setting learning rate to 0.0003598417.
390/390 [==============================] - 7s 19ms/step - loss: 0.4230 - acc: 0.8490 - val_loss: 0.5619 - val_acc: 0.8132
Epoch 25/50

Epoch 00025: LearningRateScheduler setting learning rate to 0.0003465804.
390/390 [==============================] - 7s 19ms/step - loss: 0.4140 - acc: 0.8537 - val_loss: 0.5480 - val_acc: 0.8173
Epoch 26/50

Epoch 00026: LearningRateScheduler setting learning rate to 0.0003342618.
390/390 [==============================] - 7s 19ms/step - loss: 0.4150 - acc: 0.8555 - val_loss: 0.5348 - val_acc: 0.8219
Epoch 27/50

Epoch 00027: LearningRateScheduler setting learning rate to 0.0003227889.
390/390 [==============================] - 8s 19ms/step - loss: 0.4103 - acc: 0.8544 - val_loss: 0.5615 - val_acc: 0.8146
Epoch 28/50

Epoch 00028: LearningRateScheduler setting learning rate to 0.0003120774.
390/390 [==============================] - 8s 20ms/step - loss: 0.4022 - acc: 0.8579 - val_loss: 0.5377 - val_acc: 0.8185
Epoch 29/50

Epoch 00029: LearningRateScheduler setting learning rate to 0.000302054.
390/390 [==============================] - 8s 19ms/step - loss: 0.4039 - acc: 0.8556 - val_loss: 0.5503 - val_acc: 0.8212
Epoch 30/50

Epoch 00030: LearningRateScheduler setting learning rate to 0.0002926544.
390/390 [==============================] - 8s 20ms/step - loss: 0.3888 - acc: 0.8603 - val_loss: 0.5666 - val_acc: 0.8142
Epoch 31/50

Epoch 00031: LearningRateScheduler setting learning rate to 0.0002838221.
390/390 [==============================] - 8s 19ms/step - loss: 0.3918 - acc: 0.8603 - val_loss: 0.5997 - val_acc: 0.8077
Epoch 32/50

Epoch 00032: LearningRateScheduler setting learning rate to 0.0002755074.
390/390 [==============================] - 8s 19ms/step - loss: 0.3873 - acc: 0.8626 - val_loss: 0.5458 - val_acc: 0.8230
Epoch 33/50

Epoch 00033: LearningRateScheduler setting learning rate to 0.000267666.
390/390 [==============================] - 8s 19ms/step - loss: 0.3833 - acc: 0.8640 - val_loss: 0.5375 - val_acc: 0.8239
Epoch 34/50

Epoch 00034: LearningRateScheduler setting learning rate to 0.0002602585.
390/390 [==============================] - 8s 19ms/step - loss: 0.3842 - acc: 0.8640 - val_loss: 0.5320 - val_acc: 0.8246
Epoch 35/50

Epoch 00035: LearningRateScheduler setting learning rate to 0.00025325.
390/390 [==============================] - 8s 20ms/step - loss: 0.3775 - acc: 0.8646 - val_loss: 0.5658 - val_acc: 0.8191
Epoch 36/50

Epoch 00036: LearningRateScheduler setting learning rate to 0.0002466091.
390/390 [==============================] - 8s 20ms/step - loss: 0.3750 - acc: 0.8663 - val_loss: 0.5486 - val_acc: 0.8222
Epoch 37/50

Epoch 00037: LearningRateScheduler setting learning rate to 0.0002403076.
390/390 [==============================] - 8s 19ms/step - loss: 0.3716 - acc: 0.8673 - val_loss: 0.5334 - val_acc: 0.8259
Epoch 38/50

Epoch 00038: LearningRateScheduler setting learning rate to 0.0002343201.
390/390 [==============================] - 8s 20ms/step - loss: 0.3666 - acc: 0.8707 - val_loss: 0.5436 - val_acc: 0.8236
Epoch 39/50

Epoch 00039: LearningRateScheduler setting learning rate to 0.0002286237.
390/390 [==============================] - 8s 20ms/step - loss: 0.3631 - acc: 0.8707 - val_loss: 0.5401 - val_acc: 0.8262
Epoch 40/50

Epoch 00040: LearningRateScheduler setting learning rate to 0.0002231977.
390/390 [==============================] - 8s 20ms/step - loss: 0.3659 - acc: 0.8688 - val_loss: 0.5398 - val_acc: 0.8292
Epoch 41/50

Epoch 00041: LearningRateScheduler setting learning rate to 0.0002180233.
390/390 [==============================] - 8s 20ms/step - loss: 0.3558 - acc: 0.8728 - val_loss: 0.5382 - val_acc: 0.8274
Epoch 42/50

Epoch 00042: LearningRateScheduler setting learning rate to 0.0002130833.
390/390 [==============================] - 8s 20ms/step - loss: 0.3579 - acc: 0.8721 - val_loss: 0.5508 - val_acc: 0.8256
Epoch 43/50

Epoch 00043: LearningRateScheduler setting learning rate to 0.0002083623.
390/390 [==============================] - 8s 20ms/step - loss: 0.3595 - acc: 0.8727 - val_loss: 0.5399 - val_acc: 0.8320
Epoch 44/50

Epoch 00044: LearningRateScheduler setting learning rate to 0.0002038459.
390/390 [==============================] - 8s 20ms/step - loss: 0.3535 - acc: 0.8746 - val_loss: 0.5435 - val_acc: 0.8268
Epoch 45/50

Epoch 00045: LearningRateScheduler setting learning rate to 0.0001995211.
390/390 [==============================] - 8s 19ms/step - loss: 0.3516 - acc: 0.8757 - val_loss: 0.5543 - val_acc: 0.8222
Epoch 46/50

Epoch 00046: LearningRateScheduler setting learning rate to 0.0001953761.
390/390 [==============================] - 8s 20ms/step - loss: 0.3518 - acc: 0.8742 - val_loss: 0.5446 - val_acc: 0.8260
Epoch 47/50

Epoch 00047: LearningRateScheduler setting learning rate to 0.0001913998.
390/390 [==============================] - 8s 20ms/step - loss: 0.3419 - acc: 0.8765 - val_loss: 0.5313 - val_acc: 0.8299
Epoch 48/50

Epoch 00048: LearningRateScheduler setting learning rate to 0.0001875821.
390/390 [==============================] - 8s 20ms/step - loss: 0.3498 - acc: 0.8736 - val_loss: 0.5291 - val_acc: 0.8297
Epoch 49/50

Epoch 00049: LearningRateScheduler setting learning rate to 0.0001839137.
390/390 [==============================] - 8s 19ms/step - loss: 0.3417 - acc: 0.8783 - val_loss: 0.5400 - val_acc: 0.8277
Epoch 50/50

Epoch 00050: LearningRateScheduler setting learning rate to 0.000180386.
390/390 [==============================] - 8s 19ms/step - loss: 0.3435 - acc: 0.8778 - val_loss: 0.5335 - val_acc: 0.8303
Model took 388.29 seconds to train

Accuracy on test data is: 83.03
```
