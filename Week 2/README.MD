Group Members : Pranav Piyush (https://github.com/fatsoengineer/EIP_4/tree/master/Week_2)


print(score) : [0.019144815586134793, 0.9946]

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 16s 274us/step - loss: 0.5214 - acc: 0.8556 - val_loss: 0.1025 - val_acc: 0.9813
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 10s 173us/step - loss: 0.2516 - acc: 0.9261 - val_loss: 0.0615 - val_acc: 0.9871
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 10s 175us/step - loss: 0.1986 - acc: 0.9423 - val_loss: 0.0525 - val_acc: 0.9886
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 11s 176us/step - loss: 0.1718 - acc: 0.9469 - val_loss: 0.0399 - val_acc: 0.9901
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 11s 175us/step - loss: 0.1525 - acc: 0.9493 - val_loss: 0.0389 - val_acc: 0.9891
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 10s 174us/step - loss: 0.1403 - acc: 0.9513 - val_loss: 0.0301 - val_acc: 0.9916
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 10s 175us/step - loss: 0.1308 - acc: 0.9519 - val_loss: 0.0276 - val_acc: 0.9922
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 11s 175us/step - loss: 0.1241 - acc: 0.9537 - val_loss: 0.0256 - val_acc: 0.9929
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 10s 174us/step - loss: 0.1181 - acc: 0.9539 - val_loss: 0.0302 - val_acc: 0.9916
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 10s 175us/step - loss: 0.1109 - acc: 0.9570 - val_loss: 0.0239 - val_acc: 0.9934
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 11s 175us/step - loss: 0.1095 - acc: 0.9558 - val_loss: 0.0234 - val_acc: 0.9933
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 10s 174us/step - loss: 0.1081 - acc: 0.9558 - val_loss: 0.0215 - val_acc: 0.9943
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 10s 174us/step - loss: 0.1030 - acc: 0.9565 - val_loss: 0.0202 - val_acc: 0.9942
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 10s 174us/step - loss: 0.1025 - acc: 0.9563 - val_loss: 0.0211 - val_acc: 0.9936
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 10s 174us/step - loss: 0.0973 - acc: 0.9577 - val_loss: 0.0200 - val_acc: 0.9938
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 10s 173us/step - loss: 0.0966 - acc: 0.9581 - val_loss: 0.0240 - val_acc: 0.9928
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 10s 174us/step - loss: 0.0970 - acc: 0.9576 - val_loss: 0.0191 - val_acc: 0.9945
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 11s 175us/step - loss: 0.0940 - acc: 0.9579 - val_loss: 0.0195 - val_acc: 0.9944
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 10s 172us/step - loss: 0.0946 - acc: 0.9585 - val_loss: 0.0201 - val_acc: 0.9939
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 10s 172us/step - loss: 0.0950 - acc: 0.9565 - val_loss: 0.0191 - val_acc: 0.9946

----------------------------------------------------------------------------------------------------------------

# Strategy

- In the initial time, we tried reducing the no of layers keeping in mind the kernel size be same as before, like 16, 32. But didn't get high accuracy. If we try to increase the kernel size, the no of parameters would sky-rocket.
Also, if to accomoddate more number of higher kernel size to restrict no of parameters, if we try to reduce no of layers, the accuracy went down.

- So, we tried to restict the kernel size to 10, 16 and increase the no on layers if necessary, for the number of parameters not to exceed 15,000 and get the desired result, which we acheived.

- Also, in notebook 8, 1x1 convolution was done before maxpooling, we moved it after maxpooling. 
