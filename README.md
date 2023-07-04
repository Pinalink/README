# README
## How I tuned my parameters to optimize the neural network engine.

  I tried using different filters for both 2D convolutions(1st conv, 2nd conv). Among the combination of (1st conv, 2nd conv) = (relu,relu)(giving accuracy=97.20%), (relu,tanh)(giving accuracy=5.37%), (sigmoid,relu)(giving accuracy=98.82%) and (sigmoid,tanh)(giving accuracy=99.16%). Interestingly (sigmoid,tanh) gave the best accuracy among these four combinations at 99.16% while (relu,tanh) astonishingly gave the worst result at an accuracy of 5.37%, a very bad result.
  Next I tried the filte size from (1st conv, 2nd conv)=(3*3, 5*5) (giving accuracy=99.16%) to (5*5, 3*3) (giving accuracy=97.59%).
  Next I changed the number of layers of convolution from (1st conv, 2nd conv)=(64,128)(giving accuracy=99.16%) to (128,64) (giving accuracy=93.94%) and (64, 32)(giving accuracy=97.42%). So in this case, less number of layers i.e. (64, 32) gave a better result. So I tested  (32, 64)(giving accuracy=98.28%) but the result is worse than (64,128)(giving accuracy=99.16%).
  Next I checked the dropout rate from 0.25 (giving accuracy=99.16%) to 0.35  (giving accuracy=5.39%) and 0.15  (giving accuracy=98.60%).
  
The program submitted with parameters having highest accuracy(99.16%) but after rerunning it again for a couple of times, the accuracy rate dropped to 98.41% and 96.38%.
