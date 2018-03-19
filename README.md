# deep-neural-network

1.vanishing gradient:
The main benefit of a very deep network is that it can represent very complex functions. 
It can also learn features at many different levels of abstraction, from edges (at the lower layers) 
to very complex features (at the deeper layers). 
However, using a deeper network doesn’t always help.

 A huge barrier to training them is vanishing gradients: 
 very deep networks often have a gradient signal that goes to zero quickly, thus making gradient descent unbearably slow. 
 More specifically, during gradient descent, as you backprop from the final layer back to the first layer, 
 you are multiplying by the weight matrix on each step,and thus the gradient can decrease exponentially quickly to zero 
 (or, in rare cases, grow exponentially quickly and “explode” to take very large values). 
 
 越是靠前的网络层，∂C/∂b1包含的乘积项越多，使得其值越小，对应网络层的学习速率越低。至此解释了vanishing gradient现象发生的原因。
