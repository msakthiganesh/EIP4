Group Members : Pranav Piyush (https://github.com/fatsoengineer/EIP_4/tree/master/Week_2)


Project Score: [0.018001809058812067, 0.9941]

Train on 60000 samples, validate on 10000 samples Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003. 60000/60000 [==============================] - 9s 147us/step - loss: 0.2129 - acc: 0.9322 - val_loss: 0.0526 - val_acc: 0.9821 Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503. 60000/60000 [==============================] - 7s 114us/step - loss: 0.0676 - acc: 0.9790 - val_loss: 0.0537 - val_acc: 0.9828 Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0496 - acc: 0.9844 - val_loss: 0.0367 - val_acc: 0.9881 Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586. 60000/60000 [==============================] - 7s 110us/step - loss: 0.0434 - acc: 0.9864 - val_loss: 0.0298 - val_acc: 0.9909 Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0386 - acc: 0.9877 - val_loss: 0.0325 - val_acc: 0.9901 Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0354 - acc: 0.9889 - val_loss: 0.0242 - val_acc: 0.9929 Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0329 - acc: 0.9894 - val_loss: 0.0246 - val_acc: 0.9926 Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0294 - acc: 0.9902 - val_loss: 0.0220 - val_acc: 0.9931 Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0284 - acc: 0.9910 - val_loss: 0.0219 - val_acc: 0.9933 Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0270 - acc: 0.9909 - val_loss: 0.0219 - val_acc: 0.9930 Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0248 - acc: 0.9920 - val_loss: 0.0179 - val_acc: 0.9941 Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0242 - acc: 0.9922 - val_loss: 0.0222 - val_acc: 0.9929 Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0228 - acc: 0.9927 - val_loss: 0.0207 - val_acc: 0.9945 Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0209 - acc: 0.9933 - val_loss: 0.0214 - val_acc: 0.9940 Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0220 - acc: 0.9930 - val_loss: 0.0222 - val_acc: 0.9933 Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825. 60000/60000 [==============================] - 7s 111us/step - loss: 0.0208 - acc: 0.9932 - val_loss: 0.0181 - val_acc: 0.9945 Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0196 - acc: 0.9938 - val_loss: 0.0173 - val_acc: 0.9949 Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0183 - acc: 0.9940 - val_loss: 0.0193 - val_acc: 0.9944 Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718. 60000/60000 [==============================] - 7s 113us/step - loss: 0.0184 - acc: 0.9939 - val_loss: 0.0173 - val_acc: 0.9951 Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869. 60000/60000 [==============================] - 7s 112us/step - loss: 0.0172 - acc: 0.9941 - val_loss: 0.0180 - val_acc: 0.9941 <keras.callbacks.History at 0x7ff7e886b860>

----------------------------------------------------------------------------------------------------------------

# Strategy

- Initially, we tried reducing the no of layers keeping in mind the kernel size be same as before, like 16, 32. But didn't get high accuracy. If we try to increase the kernel size, the no of parameters would sky-rocket.
Also, if to accomoddate more number of higher kernel size to restrict no of parameters, if we try to reduce no of layers, the accuracy went down.

- So, we tried to restict the kernel size to 10, 16 and increase the no on layers if necessary, for the number of parameters not to exceed 15,000 and get the desired result, which we acheived.

- Also, in notebook 8, 1x1 convolution was done before maxpooling, we moved it after maxpooling. 
