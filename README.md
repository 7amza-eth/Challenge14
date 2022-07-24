## Machine Learning Trading Bot Analysis

In this analysis, 3 different ML bots were modeled and compared to show the differnce that various parameters have on their performance.

## Results & Summary

### Baseline Model
![Baseline Model](/Resources/Base%20model%20returns.png) <br>
As shown in the image above, the baseline model performed slighly better than actual markert results with a return of 
~1.5x vs ~1.4x

### Adjusted Parameters Model
For this model, various combinations of training window length and the SMA input features were tested in order to improve on the baseline results. Increasing the training window did increase the returns, but during testing when the SMAs were adjusted, it led to either a loss in returns or no gain. Based on these tests, it was decided to use a 20 month training window while keeping the 4 & 100 SMA inputs

![Large Window Model](/Resources/large%20training%20window%20model%20returns.png) <br>
For this model, the returns were even greater than the baseline model at ~1.9x

### MLPClassifier Model
For this model, the training window length was returned back to the same 3 month window as the baseline. The algorithm used was a multi-layer perceptron neural network.

![MLPC Model](/Resources/MLPC%20model%20returns.png) <br>
The MLPC returns greatly outsized both the adjusted parameters and baseline models reaching a peak of ~2.5x and ending with a cumulative return of ~2x

## Dependencies
Pandas, Numpy, Pathlib, hvplot, matplotlib, sklearn