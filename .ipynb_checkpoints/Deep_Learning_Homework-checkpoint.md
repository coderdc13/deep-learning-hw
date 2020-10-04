# Deep Learning Homework


# Introduction

This assignment calls for leveraging recurrent neural networks in the comparison of prediction models for bitcoin prices. Recurrent neural networks in general may have different structures and applications (https://stanford.edu/~shervine/teaching/cs-230/cheatsheet-recurrent-neural-networks). Also, one can consider the long short term memory (LSTM) recurrent neural network (RNN) as a methodology that "allows learning of long-term dependencies" (http://pages.cs.wisc.edu/~shavlik/cs638/lectureNotes/Long%20Short-Term%20Memory%20Networks.pdf). LSTM RNNs have been leveraged for predictive financial models (http://cs230.stanford.edu/projects_fall_2019/reports/26254244.pdf).



## Window Sizes and Loss


### Closing Price Model


Window Size 10


5/5 [==============================] - 0s 13ms/step - loss: 0.0616
0.06157752126455307

Window Size 9


5/5 [==============================] - 0s 11ms/step - loss: 0.0607
0.06065821647644043

Window Size 8


6/6 [==============================] - 0s 5ms/step - loss: 0.0573
0.057325515896081924

Window Size 7


6/6 [==============================] - 0s 10ms/step - loss: 0.0584
0.05839494243264198

Window Size 6


6/6 [==============================] - 0s 7ms/step - loss: 0.0547
0.05467987060546875

Window Size 5


6/6 [==============================] - 0s 10ms/step - loss: 0.0490
0.04902857914566994

Window Size 4


6/6 [==============================] - 0s 5ms/step - loss: 0.0448
0.04480021074414253

Window Size 3


6/6 [==============================] - 0s 4ms/step - loss: 0.0392
0.039153698831796646

Window Size 2


6/6 [==============================] - 0s 5ms/step - loss: 0.0323
0.03228790685534477

Window Size 1


6/6 [==============================] - 0s 3ms/step - loss: 0.0267
0.026739951223134995



### Fear and Greed (FNG)


Window Size 10


5/5 [==============================] - 0s 5ms/step - loss: 0.1219
0.12194053828716278

Window Size 9


5/5 [==============================] - 0s 5ms/step - loss: 0.1434
0.14338549971580505

Window Size 8


6/6 [==============================] - 0s 5ms/step - loss: 0.1332
0.13317695260047913

Window Size 7


6/6 [==============================] - 0s 12ms/step - loss: 0.1230
0.12296931445598602

Window Size 6


6/6 [==============================] - 0s 4ms/step - loss: 0.1165
0.11649595201015472

Window Size 5


6/6 [==============================] - 0s 4ms/step - loss: 0.1211
0.12107281386852264

Window Size 4


6/6 [==============================] - 0s 4ms/step - loss: 0.1200
0.11998255550861359

Window Size 3


6/6 [==============================] - 0s 3ms/step - loss: 0.1138
0.11377636343240738

Window Size 2


6/6 [==============================] - 0s 5ms/step - loss: 0.1138
0.1137816309928894

Window Size 1


6/6 [==============================] - 0s 3ms/step - loss: 0.1117
0.11165456473827362





> Which model has a lower loss?
From the data above for loss, one can note that the closing price model has a lower loss.
>
> Which model tracks the actual values better over time?
In terms of tracking values over time, from the data in the graphs, one can see that the closing price model tracks the actual values better over time.
>
> Which window size works best for the model?
The data for loss and window size are provided above. After running each of the models for each window size from ten to one, the losses were recorded. In general, the loss was the least with the smallest window size (window size equal to one) for each model. It is worthy to note that with window size equal to one for each model, the loss was less for the student author than for the starter code (closing price model was loss 0.0267 for the student author and 0.0487 for the starter code, and fear and greed model was loss 0.1117 for the student author and 0.1911 for the starter code).