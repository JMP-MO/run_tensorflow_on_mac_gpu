# Run TensorFlow on Apple mac M-series 🍟

The TensorFlow machine learning framework is supposed to automatically detect and prioritise the use of GPUs over CPUs. <br>
However, when using Tensorflow on a M-series (Apple Silicon) mac I have found that TensorFlow does not automatically detect and use your Apple GPU; increasing training time significantly. 

* I have listed the steps below to create an environment which will enable TensorFlow to recognise and use Apple's GPUs on M-series chips.
* I have also included a jupyter notebook with an example comparing Apple's GPU and CPU (using a M1-Pro laptop) in a small TensorFlow ML project.


### 📦 Environment requirements 

I used Conda to create a new envirnment with python included. Then manually installed the following pip packages. Then manually added other conda packages I needed. I experimented with creating a YAML file with these instructions, however have continued to find issues with package conflicts when automating this process, but this manual method worked.  

**Step-bystep Environment Instructions:**

1. Create a new environment with python.
2. pip install tensorflow-macos
3. pip install tensorflow-metal
4. conda install your other packages such as jupyter, pandas etc...

Tensorflow should now automatically use your Mac M-series GPU if it can locate them.
